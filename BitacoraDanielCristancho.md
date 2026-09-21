# Bitácora Personal — Daniel Cristancho

> Registro individual de trabajo. Bitácora del equipo: [BitacoraGrupal.md](./BitacoraGrupal.md)

## [13/08/2026]

**¿Qué hice?**
- desarrolle los CU-001 – CU-005 Boletería / Entradas y CU-021 – CU-023 Parqueadero (reservas y accesos)

**¿Qué aprendí?**
- Aprendi a estructurar los casos de uso siguiendo un formato estándar (actores, flujo básico, alternos, excepciones, pre/post-condiciones) identificando los flujos alternos y de excepción a partir de las ramificaciones del proceso (pago rechazado, QR inválido, cupo no disponible, etc.)


**Dificultades o dudas**
- Falta validar con el equipo si Parqueadero debe manejar su propia base de datos o compartir la de Logística

**Próximos pasos**
- Iniciar con el desarrollo del documento SAD

---

## [19/09/2026]

**¿Qué hice?**
- Implementé el backend de mis cinco casos de uso (**CU-001 a CU-005**)
- como dos módulos hermanos del de reventa de Samuel, 14 rutas nuevas; el contrato pasó de 8 a 20.
- **CU-001 (Compra)**: la separé en dos peticiones, reservar y pagar, con un
  plazo entre las dos. Así nadie paga por un cupo que ya se llevó otra persona.
  Añadí un estado `PAGANDO` para que el barrido de reservas vencidas no libere
  el cupo mientras la pasarela está procesando el cobro.
- **CU-002 (Validar QR)**: doble barrera contra el doble ingreso — un `UPDATE`
  condicional sobre el estado de la entrada y un `UNIQUE (entrada_id)` en la
  tabla de ingresos. Para el modo sin conexión, el dispositivo descarga hashes
  SHA-256 de los QR válidos, no los códigos, para que un teléfono robado en la
  puerta no sirva para entrar.
- **CU-003 (Cancelaciones)**: elegí anular primero y reembolsar después. El
  orden contrario deja al cliente con el dinero y una entrada válida si falla
  el segundo paso; así, si la pasarela rechaza, las entradas vuelven a ser válidas.
- **CU-004 (Promociones)** y **CU-005 (Cartelera)**: el descuento lo calcula
  siempre el servidor sobre la compra guardada, y la cartelera quedó pública y
  de solo lectura.
- Dos migraciones escritas a mano: 6 tablas nuevas y 3 ampliadas.
- 336 pruebas unitarias pasando (antes eran 183) y cobertura de 79,3 % a 85,9 %.
  Además probé cada camino de las fichas contra Postgres, Redis, RabbitMQ y la
  pasarela reales en Docker.

**¿Qué aprendí?**
- A controlar la concurrencia con un solo `UPDATE` condicional
  (`SET x = x + n WHERE x + n <= limite`) en vez de leer y después escribir.
  Entre la lectura y la escritura cabe otra petición, y las dos creerían haber
  tomado el último cupo. Lo medí: 20 intentos simultáneos sobre un cupón de 5
  usos dejaron exactamente 5.
- Que las reglas que nunca pueden romperse deben vivir en el motor de base de
  datos como `CHECK` e índices únicos, no en el código. Un `CHECK` sobrevive a
  un bug, a un `INSERT` hecho a mano y a un servicio futuro que no conozca las reglas.
- Qué es una clave de idempotencia y por qué importa: usando
  `compra:intentosRechazados`, reintentar un cobro sin respuesta no cobra dos
  veces, pero reintentar tras un rechazo sí es un cobro nuevo.
- Que cuando hay dinero de por medio, el **orden** de las operaciones es una
  decisión de arquitectura, no un detalle de implementación.

**Dificultades o dudas**
- Las fichas no fijan ni el plazo de la reserva ni la política de reembolso.
  Tuve que proponer valores (10 minutos; 100 % con 7 días o más, 50 % entre 48 h
  y 7 días) y dejarlos configurables por `.env`. Falta validarlos con el equipo.
- La cartelera pública es una excepción a RNF-06, que pide token en todo
  endpoint de negocio. La acoté a solo lectura, pero es una decisión del equipo.
- Tuve que modificar cinco archivos del módulo de reventa de Samuel (la interfaz
  de pagos necesitaba `reembolsar()`). Los cambios son aditivos y sus pruebas
  siguen pasando, pero conviene que él los revise en el PR.

**Próximos pasos**
- Conectar el portal web y la app móvil, que hoy siguen con datos de prueba.
- Probar las rutas de punta a punta a través del gateway.
- Abrir el PR hacia `develop`.

---

## [21/09/2026]

**¿Qué hice?**
- Revisé el código archivo por archivo antes de commitear, en vez de dar por
  bueno que las pruebas en verde significaran que todo estaba bien. Salieron
  tres cosas que las pruebas no detectaban.
- **Corregí un fallo de diseño en la migración de la cartelera**: la columna
  `estado` de los eventos quedaba con `DEFAULT 'PUBLICADO'` de forma permanente.
  El valor por defecto solo hacía falta para rellenar las filas que ya existían;
  dejarlo puesto significaba que un evento insertado sin estado se publicaría
  solo, con entradas a la venta. Le añadí el `DROP DEFAULT` y quité el default
  gemelo que tenía la entidad de TypeORM.
- **Encontré que se pueden vender más entradas que el aforo del recinto** si las
  localidades de un evento se configuran mal, y que hoy eso solo se detecta en
  la puerta, con el cliente ya allí. La validación corresponde a CU-026
  (servicio de Eventos, de Samuel), así que no la puedo hacer en mi servicio.
  Reformulé el mensaje de CU-002B, que prometía una espera imposible (el
  contador de asistentes nunca baja porque no se registran salidas), y añadí una
  alerta en el log para que quede rastro cuando ocurra.
- **Detecté que no existe proceso de conciliación** para los tres caminos en que
  la pasarela no responde: quedan registrados en la base y en el log, pero nadie
  los revisa después. El SAD pide una cola de reconciliación que no está hecha.
- Apliqué dos avisos de SonarQube (optional chaining) y arreglé un typo en un
  mensaje de cara al usuario.
- Commit y push de los 58 archivos a `feature/daniel`.

**¿Qué aprendí?**
- Que un valor por defecto es una decisión de seguridad. Ante un dato que falta,
  el sistema debe quedarse en el estado menos expuesto, no en el más cómodo:
  mejor que un `INSERT` incompleto falle a gritos que que publique un evento.
- Que las pruebas también protegen la documentación. Al limpiar comentarios
  borré sin querer el marcador "(CU-003D)" de un mensaje, y una prueba que
  comprobaba justo esa trazabilidad se puso en rojo. Sin ella, el vínculo entre
  el código y la ficha se habría perdido en silencio.
- A razonar dónde **corresponde** poner una validación, y no solo dónde es
  cómoda. La del aforo es del servicio de Eventos porque él es dueño del dato
  (ADR-01); lo que me toca a mí es defenderme de recibirlo mal.
- Que revisar código con calma encuentra cosas que ni el compilador, ni 336
  pruebas, ni SonarQube detectan, porque no son errores de código sino
  decisiones equivocadas.

**Dificultades o dudas**
- Los tres hallazgos cruzan la frontera de mi servicio y hay que decidirlos en
  equipo: la validación del aforo en CU-026, la cola de conciliación, y si vale
  la pena registrar las salidas del recinto.

**Próximos pasos**
- Abrir el PR hacia `develop` y avisar a Samuel de los cinco archivos suyos.
- Llevar los tres hallazgos a la reunión de equipo.
- Conectar el portal web y la app móvil al backend.
