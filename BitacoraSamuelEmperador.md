# Bitácora Personal — Samuel Emperador

> Registro individual de trabajo. Bitácora del equipo: [BitacoraGrupal.md](./BitacoraGrupal.md)

## [31/07/2026]

**¿Qué hice?**
- Participé en la Sesión N.º 1 del equipo (11:00–11:30 am, presencial): presentamos la idea de proyecto que pedía la Clase 1 y elegimos **"Sistema Integral de Gestión de Eventos"**.
- Ayudé a definir el enfoque general de desarrollo (alcance y módulos principales: boletería/entradas, personal, pedidos, logística, parqueadero).
- Empecé a levantar el borrador de mis primeros casos de uso.

**Próximos pasos**
- Seguir levantando casos de uso de mi módulo para consolidarlos en la Sesión 2.

---

## [06/08/2026]

**¿Qué hice?**
- Participé en la Sesión N.º 2 del equipo (11:00–11:30 am, presencial): revisamos los borradores de casos de uso de cada integrante/módulo y cerramos el listado completo en `Submission/CU_eventos_completo.xlsx`.
- Ayudé a estandarizar el formato de caso de uso entre los distintos módulos, para que todos siguieran la misma plantilla.

**Próximos pasos**
- Esperar la retroalimentación del profesor sobre el listado de casos de uso.

---

## [13/08/2026]

**¿Qué hice?**
- Participé en la Sesión N.º 3 del equipo (11:00–11:30 am, presencial): revisamos las recomendaciones del profesor sobre el listado de casos de uso y aplicamos los cambios pedidos, dejando esa versión como la definitiva antes de pasar a la arquitectura.
- Empece a investigar sobre la propuesta arquitectonica y el diagrama C4

**Próximos pasos**
- Empezar el diseño de la propuesta arquitectónica y el diagrama C4 con base en la versión final de los casos de uso.

---

## [19/08/2026]

**¿Qué hice?**

- Con apoyo de asistente de IA, hice una revisión y reorganización a fondo de `Submission/CU_eventos_completo.xlsx`:
  - Renumeré los 25 casos de uso a `CU-001`–`CU-025` por bloque (Boletería, Personal, Pedidos, Logística, Parqueadero), corrigiendo IDs y referencias cruzadas rotas entre ellos.
  - Amplié el flujo básico de 13 CU a 8–10 pasos para cumplir el mínimo exigido en la Clase 1, y corregí un error de columna en CU-024.
  - Añadí 7 casos de uso nuevos (`CU-026`–`CU-032`) para cerrar huecos de CRUD que faltaban (gestión de eventos, cuentas de usuario, roles/permisos, recintos/zonas, proveedores, pagos/conciliación, reportes) — el listado quedó en **32 casos de uso**.
- Detecté y sincronicé 5 hojas duplicadas del spreadsheet que habían reaparecido por una sincronización de OneDrive, para que no contradijeran a los CU ya corregidos.
- Actualicé y organicé `Cronograma.md` con la planificación semana a semana del proyecto hasta fin de semestre.
- Documentación de la prouesta arquitectónica.
- Eleboración de la primera version de la diagramación C4.

**Próximos pasos**
- Revisar con cada integrante los casos de uso que le correspondan (en especial los 7 nuevos) antes de la entrega.
- Seguir con la propuesta arquitectónica y los diagramas C4.

---

## [20/08/2026]

**¿Qué hice?**
- Participé en la Sesión N.º 4 del equipo (11:00–11:30 am, presencial): Tuvimos una retroalimentacion sobre la primera version de los diagramas C4.
- Cree el repositorio con las bitacoras personal y la bitacora grupal con una plantilla para tener todo el proceso del proyecto documentado y organizado.
- Actualización de la bitacora grupal con las reuniones grupales que hemos tenido hasta el dia de hoy.
- Actualización de mi bitacora personal con todo el trabajo que he realizado hasta el dia de hoy.
- Distribución de los casos de uso y envio del mismo al profesor.

**Próximos pasos**
- Mantener la Bitácora Arquitectónica actualizada con cada avance técnico, sin reescribir entradas pasadas.
- Hacer los cambias que nos dijo el profesor en la retroalimentación de los diagrmas C4.

---

## [22/08/2026] 

**¿Qué hice?**
- Revisé el documento de Diagramas C4 (C4Diagrams.tex) completo contra el checklist oficial de c4model.com (https://c4model.com/diagrams/checklist).
- Rehice los 6 diagramas (Contexto, Contenedores, Componentes, Panorama de Sistemas, Secuencia y Despliegue) en draw.io (app.diagrams.net), aplicando la retroalimentación del profesor: cada caja ahora muestra nombre, tipo/tecnología entre corchetes y una breve descripción, y el antiguo Diagrama Dinámico se reemplazó por un Diagrama de Secuencia UML con líneas de vida, mensajes numerados y barra de activación.
- Exporté los 6 diagramas como imágenes PNG y guardé también los archivos fuente .drawio en Work/Diagrams/, para poder editarlos más adelante.
- Mejoré el formato del documento en LaTeX (tablas con encabezado repetido en cada página, texto alineado a la izquierda en vez de justificado, imágenes que no se salen de la página).
- Recompilé C4Diagrams.tex sin errores ni advertencias y actualicé el PDF final en Submission/C4Diagrams.pdf. 

**Próximos pasos** 
- Mostrar los nuevos avances al profesor y al equipo para escuchar nuevas sugerencias.
- Revisar si el diagrama de despliegue en Kubernetes coincide con la plataforma que el equipo realmente va a usar.
- Mantener la Bitácora Arquitectónica actualizada con cada avance técnico, sin reescribir entradas pasadas.

---

## [25/08/2026]

**¿Qué hice?**
- Hice el cambio de la plantilla del documento SAD de word a latex y tambien se elaboro la primera version de este mismo.

**Próximos pasos** 
- Mostrar al profesor la primera versión y tomar su retroalimentación.

---

## [27/08/2026]

**¿Qué hice?**
- Crear la rama Develop y mi rama personal feature/samuel
- Crear estructura basica de la aplicación

**Próximos pasos** 
- Empezar con la implementación de la aplicación.

---

## [31/08/2026]

**¿Qué hice?**
- Generé los 6 diagramas C4 del sistema (Contexto, Contenedores, Componentes, Panorama de Sistemas, Secuencia y Despliegue) con la herramienta [archify](https://github.com/tt-a1i/archify.git), como HTML interactivos (pan/zoom, tema claro/oscuro), en `Documentation/Work/Diagrams/Archify/`.
- Cree una aplicación base de la apliacion movil de cliente.
- Limpié `Documentation/Work/` para que solo tenga fuentes (`.tex`, `.md`, `Diagrams/`): moví los PDF compilados a `Documentation/Submission/`, eliminé los subproductos de LaTeX sueltos (`.aux .log .out .toc .fls .fdb_latexmk`) y actualicé `.gitignore` más un `README.md` con el flujo de compilación, para que no se vuelva a acumular basura de compilación.

**Próximos pasos**
- Conectar los servicios mock del Portal Web Cliente al API Gateway real cuando el backend esté disponible.
- Actualizar `C4Diagrams.tex`/`DescripcionArquitecturaSoftware.tex` para que coincidan con los diagramas de archify (4 apps, 6 microservicios).
- Revisar con el equipo el PR que hice hacia el main desde la rama develop.
- Revisar documentacion si podemos tener una unica aplicacion movil para los usuarios de cliente y personal.

---

## [02/09/2026]

**¿Qué hice?**
- Verifique como poder asignar acceso a diferentes aplicaciones despues del login por el rol que tenga cada usuario, en nuestra aplicacion movil.
- Version 0.1 de la aplicacion movil la cual solo tiene plasmado la idea de como sera nuestra aplicacion y cuales seran las funcionalidades.

**Próximos pasos**
- 

---

## [12/09/2026]

**¿Qué hice?**
- Version 2 de la pagina web siguiendo el mismo diseño de la aplicacion movil (SOLO FRONTEND).
- Toma de decision sobre lenguaje para el backend.

---

## [14/09/2026]
 
**¿Qué hice?**
- Implementé el backend completo de CU-006 (Gestión del Mercado Secundario de Entradas) como microservicio NestJS (ADR-09) sobre PostgreSQL, Redis y RabbitMQ, cubriendo los 13 pasos del flujo básico y los nueve caminos alternos y de excepción (CU-006A a CU-006I).
- El flujo quedó end-to-end: publicación de la entrada con tope de precio, consulta del mercado, checkout con bloqueo distribuido en Redis (ADR-03), cobro contra una pasarela de pago simulada en contenedor, transferencia de propiedad con reemisión del QR e historial auditable, publicación del evento ENTRADA_TRANSFERIDA en RabbitMQ (ADR-10) con sus consumidores de notificación y liquidación, y expiración programada de las publicaciones.
- Agregué al modelo de datos tres tablas que el SAD §12 no contemplaba — transacciones_reventa, historial_propietarios y eventos_referencia —, necesarias para cumplir la post-condición 3 del caso de uso y el RNF-11.
- Conecté la app móvil a la API real (las dos pestañas de reventa) y publiqué los contratos en App/shared/ como OpenAPI y JSON Schema.
- Verificación: 169 pruebas unitarias con 76,5 % de cobertura (RNF-18 pide 70 %) y cuatro suites de integración contra infraestructura real.
- Corregí cinco defectos de corrección que destapó una revisión posterior. El más grave estaba justo en el invariante que este caso de uso demuestra: el checkout verificaba que existiera un bloqueo sobre la publicación, pero no que fuera del comprador que estaba pagando; si la reserva caducaba y otro la tomaba, ambos podían pagar. Medido: dos cobros, dos transferencias y dos códigos QR sobre una sola entrada. Lo cerré con tres barreras encadenadas (bloqueo, verificación de titularidad y UPDATE condicional) y dejé como pruebas de regresión los dos escenarios que lo reproducían.
 
**Próximos pasos**
- Llevar la cobertura de pruebas de integración de CU-006 al 100 % antes del 20/09.
- Documentar ADR-09 (NestJS como stack de backend) y ADR-10 (mensajería con RabbitMQ), y actualizar el modelo de datos del SAD §12 con las tres tablas nuevas.
- Incluir en el guion de demo el escenario de doble cobro (antes/después de la corrección) como evidencia cuantitativa del bloqueo distribuido, junto con los resultados de PoC-01.
 
---
 
## [17/09/2026]
 
**¿Qué hice?**
- Implementé backend completo **CU-027 (Cuentas de Usuario)**: microservicio NestJS (Administración) sobre PostgreSQL/RabbitMQ — registro scrypt, verificación correo, login RS256, bloqueo fuerza bruta, recuperación contraseña, edición perfil, admin cuentas (activar/desactivar/eliminar). Tablas nuevas: `sesiones`, `tokens_cuenta`, `auditoria_cuentas`. **ADR-01**: anonimiza al eliminar (FK lógicas en otras BD). **Usabilidad**: login tiempo constante con hash señuelo.
- Conecté **CU-006 → CU-027 (RNF-06)**: tokens RS256 en lugar de `X-Usuario-Id`, sesiones Redis (ADR-03), renovación access 15min / refresh 30d con rotación y detección reuso sin almacenar tokens. App móvil (llavero) + portal web (cookie HttpOnly, tema oscuro).
- Verificación: 7 suites integración CU-027, 11 rutas CU-006 → 401 sin token, E2E iPhone/Chrome. **Disponibilidad**: login 76→114 req/s, consulta 4.9s→<1s, PG caído → 503 en 3s, `/salud` chequea BD, recuperación 1.3s (RNF-04 ≤30s).
- Defectos por medición: logout no propagaba (TypeORM `RETURNING`), deadlock 2 admins desactivándose → 500. Endurecí pruebas primero.
- Pendientes: API Gateway (ADR-02), cobertura unitaria Admin 8% vs 70% RNF-18, reventa portal (RNF-14), SAD desactualizado.
- **API Gateway (ADR-02)**: Nginx punto único entrada, subpetición a `/sesiones/verificar` del servicio Administración, microservicios validan por su cuenta (prueba falsifica cabecera → 401). App/portal usan una sola dirección.
- **SRS**: 66 págs generadas desde `CU_eventos_completo.xlsx` (fuente de verdad), tabla 18 RNF compartida con SAD.
- **ADR-11**: autenticación RS256 vs HS256 (evita fabricación tokens admin), revocación Redis, dos tokens.
- **Desplegabilidad**: `iniciar.sh` levanta 10 contenedores en 2m14s, 2 computadores (`--rol datos/servicios`), CI/CD (8 jobs PR, CD publica en ghcr.io etiquetado rama/commit, verifica arranque).
- **Medición atributos**: catálogo mercado secundario p95 150ms (umbral 500ms RNF-07), 1417 req/s sin fallos. 2 réplicas en 1 máquina empeora p95 a 198ms (compiten núcleos/BD) — confirma necesidad 2 máquinas. 2 réplicas sobreviven caída 1 (20/20 ok).
- **Cobertura integración real**: Administración 94.95%, Entradas 85.87% sentencias (c8). `npm test:cov` (90.9%) engañoso: Jest mide solo archivos tocados (4.9% real).
- **CU-018**: corregido tope diario horas (comparaba contra acumulado vida), ligado a CU-027 (empleado→cuenta, admin da alta, app pide área al login en vez de mapa local).
 
**Próximos pasos**
- Continuar backend y pruebas de integración con Diego
- Congelamiento 21/09

---

## [19/09/2026]

**¿Qué hice?**
- Nueva versión de CU-018 sobre el login real (CU-027): cliente de logística de la app móvil, rutas del gateway, `iniciar.sh` y `docker-compose.remoto.yml` para dos computadores ([`2dbee9a`](https://github.com/Emperador24/HEXACORE/commit/2dbee9a)).
- Arreglé el CI de Eventos/Emergencias en dos frentes.
  - El lock había perdido una entrada de `typescript` que npm 10 (el del pipeline) exige y npm 11 no.
  - La fusión hacía que `npm test` intentara correr las 34 pruebas de integración en el CI, que no tiene PostgreSQL ni RabbitMQ.

  Commits: [`b9dc700`](https://github.com/Emperador24/HEXACORE/commit/b9dc700), [`5f70333`](https://github.com/Emperador24/HEXACORE/commit/5f70333).
- La prueba de integración de la app fallaba de forma intermitente por `setState` sobre pantallas ya cerradas. Corregido ([`fc26187`](https://github.com/Emperador24/HEXACORE/commit/fc26187)).
- Corregí el tope diario de horas (CU-017/018). Comparaba contra el acumulado de toda la vida, así que quien más trabajaba quedaba inasignable para siempre. También medí la cobertura de integración ([`ba65b42`](https://github.com/Emperador24/HEXACORE/commit/ba65b42)).
- PR #24 y #25 a `develop`.

**Próximos pasos**
- Pipeline de entrega continua (CD) y publicación de imágenes.

---

## [20/09/2026]

**¿Qué hice?**
- Pipeline de CD:
  - imágenes del gateway y de los servicios publicadas en ghcr.io en cada push a `develop`/`main`, etiquetadas por rama y por commit;
  - comprobación de que lo publicado arranca;
  - publicación para **amd64 y arm64** ([`65624a4`](https://github.com/Emperador24/HEXACORE/commit/65624a4), [`e57868c`](https://github.com/Emperador24/HEXACORE/commit/e57868c)).
- Validé el multiarquitectura. Descargué las imágenes sin credenciales en un Mac arm64 y levanté el sistema completo con `./iniciar.sh --registro` en 2 min 32 s ([`748e553`](https://github.com/Emperador24/HEXACORE/commit/748e553)).
- El sistema ya arranca sin Node instalado: el portal pasa a contenedor y los datos de ejemplo a SQL ([`87b8bb2`](https://github.com/Emperador24/HEXACORE/commit/87b8bb2)).

**Próximos pasos**
- Conectar la reventa del portal web al backend real.
- Pruebas de integración de los servicios que no tienen.

---

## [21/09/2026]

**¿Qué hice?**
- Conecté el mercado de reventa del portal web al backend real (CU-006). Antes publicaba y compraba sobre una lista en memoria del navegador; ahora usa el gateway con el mismo recorrido que la app ([`6d8e97e`](https://github.com/Emperador24/HEXACORE/commit/6d8e97e)).
- PR #26 a `develop`; revisé y fusioné los PR #27, #28, #30 y #31 de Sebastián y Daniel, y el #29 de `develop` a `main`.

**Próximos pasos**
- Congelamiento: pruebas de integración, CI y despliegue en dos computadores.

---

## [22/09/2026]

**¿Qué hice?** (día del congelamiento; 22 commits, desde la madrugada)
- **Pruebas de integración.**
  - **CU-011:** no tenía ninguna; agregué 33 comprobaciones (87,4 % de cobertura de integración).
  - **Venta primaria CU-001–005:** tampoco tenía; agregué cinco suites con 75 bloques.
  - **Guardas de pago de Pedidos:** 14 bloques.
  - **Cobertura de Eventos/Emergencias:** medida por primera vez.
  - **Base propia:** las pruebas pasaron a su propia base y agregué un recolector de datos de prueba. Se habían acumulado 719 empleados y 415 turnos en la base de trabajo.
  - **CI:** ahora las ejecuta, y Pedidos entra al CI/CD.

  Commits: [`a52b23c`](https://github.com/Emperador24/HEXACORE/commit/a52b23c), [`3464307`](https://github.com/Emperador24/HEXACORE/commit/3464307), [`1d6ed3a`](https://github.com/Emperador24/HEXACORE/commit/1d6ed3a), [`08c052c`](https://github.com/Emperador24/HEXACORE/commit/08c052c), [`8b56b49`](https://github.com/Emperador24/HEXACORE/commit/8b56b49), [`b402df7`](https://github.com/Emperador24/HEXACORE/commit/b402df7), [`2747215`](https://github.com/Emperador24/HEXACORE/commit/2747215), [`bee2f77`](https://github.com/Emperador24/HEXACORE/commit/bee2f77).
- **Defectos corregidos.**
  - Una comilla en la migración de la venta primaria impedía crear seis tablas ([`528e6ba`](https://github.com/Emperador24/HEXACORE/commit/528e6ba)).
  - El orden "evento próximo" del mercado daba 500 siempre ([`a3ac0cd`](https://github.com/Emperador24/HEXACORE/commit/a3ac0cd)).
  - Las pruebas de Pedidos no arrancaban, por un problema de ESM con `@nestjs/typeorm` ([`9ea8b05`](https://github.com/Emperador24/HEXACORE/commit/9ea8b05)).
  - En logística cualquier empleado podía aprobar su propio cambio de turno; ahora se autoriza por rol ([`f54608e`](https://github.com/Emperador24/HEXACORE/commit/f54608e)).
- **Despliegue.**
  - `iniciar.sh` ahora migra y siembra: el sistema queda usable, no solo levantado ([`542df33`](https://github.com/Emperador24/HEXACORE/commit/542df33)).
  - El modo de dos computadores levantaba la capa de datos también en la máquina de servicios; quedó repartido de verdad ([`932606e`](https://github.com/Emperador24/HEXACORE/commit/932606e)).
- **Portal administrativo.** Lo conecté al backend; antes tenía tres usuarios quemados con contraseña «1234». También lo agregué al despliegue ([`2b81146`](https://github.com/Emperador24/HEXACORE/commit/2b81146)).
- **Demostración.**
  - `atributos-calidad.py` mide los cinco atributos con una sola orden ([`babc3a3`](https://github.com/Emperador24/HEXACORE/commit/babc3a3)).
  - La prueba de disponibilidad dejó de afirmar sobre una sola muestra ([`a16bcd9`](https://github.com/Emperador24/HEXACORE/commit/a16bcd9)).
  - Tácticas de seguridad y consistencia documentadas en el SAD ([`e0d4575`](https://github.com/Emperador24/HEXACORE/commit/e0d4575)).
- **App móvil.** La firma de iOS salió del proyecto para que compile en cualquier Mac ([`e422fbe`](https://github.com/Emperador24/HEXACORE/commit/e422fbe)), y el fondo difuminado se volvió más liviano ([`e38b45b`](https://github.com/Emperador24/HEXACORE/commit/e38b45b)).
- **CI en rojo.** El PR #35 se fusionó con el CI en rojo: en el runner de 2 núcleos, 1 de 900 logins no llegó a 200. Corregido con tolerancia solo en el CI ([`4a5d559`](https://github.com/Emperador24/HEXACORE/commit/4a5d559), PR #37).
- **Diapositivas.** Agregué las de la sustentación ([`cc613d5`](https://github.com/Emperador24/HEXACORE/commit/cc613d5)).
- **PRs.** #32, #35 y #38 a `develop`, y #39 de `develop` a `main`.

**Próximos pasos**
- Terminar la presentación y ensayar la sustentación.

---

## [23/09/2026]

**¿Qué hice?**
- Presentación final (`Presentacion.tex` y su PDF) llevada a `main` con el PR #42 ([`eea2ddb`](https://github.com/Emperador24/HEXACORE/commit/eea2ddb)).

**Próximos pasos**
- Sustentación de la Entrega 1 (24/09).

---

## [21/10/2026]

**¿Qué hice?**
- Registré **ADR-12**: el backend pasa de seis microservicios a tres servicios de dominio, con un Núcleo que agrupa Administración, Pedidos, Personal y Parqueaderos. La decisión salió de medir el prototipo:
  - solo uno de los seis servicios admitía réplicas;
  - dos nunca pasaron de su README;
  - las seis bases estaban en una sola instancia de PostgreSQL.

  Commit: [`aefffb5`](https://github.com/Emperador24/HEXACORE/commit/aefffb5).
- Creé el Núcleo con Administración como primer módulo y le absorbí Pedidos ([`95acc78`](https://github.com/Emperador24/HEXACORE/commit/95acc78), [`55115bc`](https://github.com/Emperador24/HEXACORE/commit/55115bc)).

**Próximos pasos**
- Probar el arranque real del Núcleo en contenedor.

---

## [22/10/2026]

**¿Qué hice?**
- Al levantar el Núcleo de verdad aparecieron cuatro fallos que ni el compilador ni las unitarias veían: migraciones apuntando a una carpeta que ya no existía, conexiones sin nombre, entre otros. Corregidos ([`4baf1ca`](https://github.com/Emperador24/HEXACORE/commit/4baf1ca)).
- La medición de atributos seguía corriendo contra la copia vieja de Administración; la apunté al Núcleo ([`677cadd`](https://github.com/Emperador24/HEXACORE/commit/677cadd)).

**Próximos pasos**
- Revisar el criterio de extracción de ADR-12.

---

## [23/10/2026]

**¿Qué hice?**
- Registré **ADR-14** (arquitectura híbrida entre SOA y microservicios). El criterio de extracción pasa de dos a cuatro condiciones, para cubrir dos casos que ADR-12 no expresaba:
  - **los transversales:** Pagos estaba duplicado en Pedidos y en Reventa, y Autenticación la usa cada petición;
  - **los que tienen almacén propio:** Catálogo, Cola virtual y Acceso QR.

  Commit: [`44cc95c`](https://github.com/Emperador24/HEXACORE/commit/44cc95c).
- Reescribí todas las vistas del SAD con ADR-14 ([`8aa4f8e`](https://github.com/Emperador24/HEXACORE/commit/8aa4f8e)).

**Próximos pasos**
- Redibujar diagramas de componentes y secuencia; limpiar los servicios sin uso.

---

## [24/10/2026]

**¿Qué hice?**
- Corregí el mapa de migración: Pagos ya tenía idempotencia ([`f2d7489`](https://github.com/Emperador24/HEXACORE/commit/f2d7489)).
- Redibujé las vistas de componentes y de secuencia, y dejé una sola versión de cada diagrama, la de ADR-14 ([`5fad606`](https://github.com/Emperador24/HEXACORE/commit/5fad606), [`8bc5505`](https://github.com/Emperador24/HEXACORE/commit/8bc5505)).
- Borré los cuatro servicios que ADR-12 dejó sin uso: 182 archivos y 572 MB duplicados ([`9467b57`](https://github.com/Emperador24/HEXACORE/commit/9467b57)).
- Recuperé en el Núcleo la tolerancia a CI de `cu027-disponibilidad`, que se había perdido al copiar la suite ([`15be90d`](https://github.com/Emperador24/HEXACORE/commit/15be90d)).

**Próximos pasos**
- Empezar las extracciones de ADR-14.

---

## [25/10/2026]

**¿Qué hice?**
- Separé dos rótulos que se tapaban en la vista de contenedores ("reserva atómica" se leía "rese…ómica" en el PDF) ([`ede4d34`](https://github.com/Emperador24/HEXACORE/commit/ede4d34)).

---

## [27/10/2026]

**¿Qué hice?**
- Apliqué las correcciones obligatorias de la revisión del profesor a la vista de contenedores ([`6eb89c2`](https://github.com/Emperador24/HEXACORE/commit/6eb89c2)):
  - el gateway enruta también a los servicios de dominio y a Acceso QR;
  - el JWT se verifica en el gateway;
  - Pagos publica PagoAprobado/PagoRechazado;
  - la pasarela confirma por webhook.
- Saqué el Catálogo a su propio microservicio (ADR-14, fase A) ([`3926e87`](https://github.com/Emperador24/HEXACORE/commit/3926e87)).

**Próximos pasos**
- Ponerlo en marcha y seguir con las extracciones.

---

## [28/10/2026]

**¿Qué hice?**
- Puse en marcha el Catálogo. Con Redis pausado la cartelera sigue respondiendo 200 mientras Ventas sale de rotación, que es justo lo que buscaba la extracción ([`1472a3f`](https://github.com/Emperador24/HEXACORE/commit/1472a3f)).
- Arreglé el apagado del Núcleo con conexiones nombradas, porque ensuciaba el cierre ordenado que pide RNF-15 ([`d938d62`](https://github.com/Emperador24/HEXACORE/commit/d938d62)).
- Saqué a servicios propios ([`dadc3f5`](https://github.com/Emperador24/HEXACORE/commit/dadc3f5), [`ec0718a`](https://github.com/Emperador24/HEXACORE/commit/ec0718a), [`90f188c`](https://github.com/Emperador24/HEXACORE/commit/90f188c), [`444eea6`](https://github.com/Emperador24/HEXACORE/commit/444eea6), [`c6d700b`](https://github.com/Emperador24/HEXACORE/commit/c6d700b)):
  - **Notificaciones**;
  - **Alimentos**, como servicio de dominio con dos réplicas fijas;
  - **Autenticación**: el Núcleo pasa a llamarse así;
  - **Pagos unificado**, con libro de idempotencia durable;
  - **Cola virtual**, construida desde cero.
- Saqué Acceso QR a su propio microservicio. Su transacción de ingreso se convirtió en una Saga ([`e71c99e`](https://github.com/Emperador24/HEXACORE/commit/e71c99e)).

**Próximos pasos**
- Extraer Postventa (CU-006).

---

## [29/10/2026]

**¿Qué hice?**
- Extraje Postventa (CU-006) a su propio servicio. Fue la extracción más cara: publicar y vender se convirtieron en Sagas, una de ellas con el pago ya cobrado ([`432cd72`](https://github.com/Emperador24/HEXACORE/commit/432cd72)).
- Renombré `entradas-mercado-secundario` a `ventas` sin renombrar la base, para no obligar a nadie a recrear su volumen. Apunté CI y CD a la carpeta nueva ([`da8b41f`](https://github.com/Emperador24/HEXACORE/commit/da8b41f), [`7a9c5da`](https://github.com/Emperador24/HEXACORE/commit/7a9c5da)).
- Dibujé la llamada de Acceso QR a Ventas en el diagrama de contenedores ([`1ca6f3f`](https://github.com/Emperador24/HEXACORE/commit/1ca6f3f)).

---

## [31/10/2026]

**¿Qué hice?**
- Registré y apliqué **ADR-15** ([`4b8cdd4`](https://github.com/Emperador24/HEXACORE/commit/4b8cdd4)):
  - el gateway valida el JWT con la clave pública y exige el turno de la Cola virtual en `POST /compras`;
  - Acceso QR valida con su propia copia de los QR;
  - Ventas y Acceso QR publican por outbox;
  - el webhook entra firmado con HMAC.
- PR #43 a `develop`.

**Próximos pasos**
- Revisar la migración a ADR-16 de Sebastián e integrarla.

---

## [02/11/2026]

**¿Qué hice?**
- Ajuste menor en el portal de clientes ([`ccc0984`](https://github.com/Emperador24/HEXACORE/commit/ccc0984)).
- Fusioné en `develop` el PR #44 de Sebastián (ADR-16: Núcleo, Boletería y Trabajador con base única por esquemas), que sustituye la topología de ADR-14.

**Próximos pasos**
- Alinear la documentación con ADR-16 y seguir con mis casos de uso sobre la arquitectura nueva.

---

## [03/11/2026]

**¿Qué hice?**
- Alineé el SAD, ADR-16, los diagramas C4, la presentación y las guías con ADR-16. Las siete vistas C4 quedaron en Archify como fuente única, y retiré de las semillas los eventos y cupones que no se podían usar ([`08ace6f`](https://github.com/Emperador24/HEXACORE/commit/08ace6f)).
- **CU-007 completo:** ficha del empleado, desactivación que cancela turnos futuros, candidatos con disponibilidad, confirmación o rechazo desde la app, y auditoría.
- **CU-026 completo,** en el nuevo módulo `eventos-recintos` del Núcleo: borrador, publicar, editar, cancelar y eliminar; aforo por recinto y zona; traslape con sugerencias; versión, historial y outbox hacia `eventos.gestion`.
- **Portal administrativo:** lo rediseñé. 831 pruebas unitarias y 93 e2e del Núcleo ([`5d21968`](https://github.com/Emperador24/HEXACORE/commit/5d21968), PR #45).
- **Datos demo:** `--datos-demo` ahora siembra recintos y eventos ([`5f287b0`](https://github.com/Emperador24/HEXACORE/commit/5f287b0)).

**Próximos pasos**
- CU-008, CU-009, CU-010, CU-024 y CU-025.

---

## [05/11/2026]

**¿Qué hice?**
- **CU-008:** cambios de turno con reemplazo, cancelación e historial.
- **CU-009:** puntualidad, estado del empleado y reporte de asistencia.
- **CU-010:** evacuación con plan, rutas, salidas, escalamiento y avisos por RabbitMQ con reintento.
- **CU-024/025:** nuevo módulo `parqueaderos` con tarifas, cobro, ocupación, alertas y redirecciones.
- Pantallas en el portal administrativo y en la app ([`e70a352`](https://github.com/Emperador24/HEXACORE/commit/e70a352)).
- Incluí CU-019 (monitoreo en vivo, de Diego) y CU-029 (recintos y zonas, de Sebastián), que quedan para revisión de sus dueños.
- La prueba de `/salud` fijaba la lista de conexiones y se rompía con cada módulo nuevo; corregida ([`ae8da7c`](https://github.com/Emperador24/HEXACORE/commit/ae8da7c)).

**Próximos pasos**
- Reserva, ingreso y espacios de parqueadero, para probar CU-024/025 de punta a punta.

---

## [07/11/2026]

**¿Qué hice?**
- Implementé CU-021, CU-022 y CU-023 (reparto de Daniel) para cerrar CU-024/025 ([`f2db59e`](https://github.com/Emperador24/HEXACORE/commit/f2db59e)):
  - reserva con bloqueo en Redis, pago y QR;
  - ingreso y salida por QR o placa, con modo sin red;
  - espacios por zona con asignación bajo bloqueo.
- CU-024A ahora sale de una reserva pagada y CU-025 cuenta los espacios reservados. Quedan para revisión de Daniel.
- Abrí el PR #47. El CI no arrancó: desde el 06/11 la cuenta tenía Actions bloqueado por facturación.

**Próximos pasos**
- Revisar a fondo mis casos de uso antes de integrarlos.

---

## [09/11/2026]

**¿Qué hice?**
- **Revisé mis casos de uso y corregí tres defectos** ([`c3fc6a6`](https://github.com/Emperador24/HEXACORE/commit/c3fc6a6)):
  1. Nadie consumía `eventos.gestion`, así que un evento publicado no llegaba a la cartelera y cancelarlo no devolvía el dinero. Ahora Catálogo, Ventas, Postventa y Acceso QR tienen su consumidor, con cola durable, DLQ y guardia de versión. Ventas devuelve el 100 % de cada compra al cancelarse el evento.
  2. Dos asignaciones simultáneas al mismo empleado pasaban las dos; ahora van en una transacción con bloqueo.
  3. `POST /logistica/turnos` admitía empleados desactivados.
- **Demo y reventa:** grabé con Playwright una demo por caso de uso y corregí dos fallos de la reventa en el portal (CU-006B y CU-006G) ([`87e7b79`](https://github.com/Emperador24/HEXACORE/commit/87e7b79)).
- **Arranque solo con Docker:** HEXACORE arranca en cualquier computador; las semillas corren en un contenedor `datos-demo`. Agregué `iniciar.ps1` para Windows ([`ec7dd0f`](https://github.com/Emperador24/HEXACORE/commit/ec7dd0f)).
- **Stripe:** pagos reales en modo de prueba, con tarjeta en Stripe Elements, webhook con firma y reembolsos. Descarté Wompi porque abrir la cuenta pedía demasiados requisitos.
- **Gmail:** correo de verificación real por SMTP, con contraseña de aplicación ([`ce0db06`](https://github.com/Emperador24/HEXACORE/commit/ce0db06)).
- **Producción:**
  - Caddy con HTTPS automático y claves JWT propias del servidor.
  - `desplegar.sh` con reversión automática.
  - Trabajo de CD que despliega cada cambio de `main` por SSH ([`9bdc469`](https://github.com/Emperador24/HEXACORE/commit/9bdc469)).
  - Elegí Oracle Cloud Always Free con DuckDNS en lugar de Azure, porque la cuenta de estudiante no permitía crear un grupo de recursos ([`3a2c1cd`](https://github.com/Emperador24/HEXACORE/commit/3a2c1cd)).
- **Verificación local:** 900 de 900 pruebas del backend, portales, app, gateway e infraestructura. Lo comprobé en proyectos de Docker aislados:
  - CU-026 de punta a punta: un evento publicado aparece en la cartelera en unos 2 s;
  - el correo llega a Mailpit;
  - el HTTPS de producción funciona;
  - un token firmado con la clave de desarrollo recibe 401.
- **Facturación de GitHub:** el uso daba US$0 netos, así que el bloqueo no venía de cobros por uso.

**Próximos pasos**
- Fusionar el PR #47 y crear la máquina de producción.

---

## [10/11/2026]

**¿Qué hice?**
- Fusioné `develop` en mi rama. Los conflictos estaban en los conteos de migraciones; quedaron 34 migraciones y 84 tablas, verificadas sobre un PostgreSQL vacío. Todas las pruebas del backend pasaron: 944 de 944, contando las de Redis ([`65f90a1`](https://github.com/Emperador24/HEXACORE/commit/65f90a13a517d67d9922d29bcf2905748d9855dc)).
- La fusión automática dejó las rutas de Stripe del gateway con una variable que `develop` había quitado, y nginx no arrancaba. Corregido y validado con `nginx -t` ([`5c641a8`](https://github.com/Emperador24/HEXACORE/commit/5c641a8)).
- Fusioné el PR #47 a `develop` (09:55). **Se fusionó con tres trabajos del CI en rojo**: e2e de parqueaderos y de convivencia de logística, guardas de revisión y transferencia histórica. Sebastián los corrigió el 11/11 en su rama.

**Próximos pasos**
- **Despliegue:**
  - crear la máquina ARM en Oracle Cloud y el dominio en DuckDNS;
  - correr `preparar-servidor.sh` y `./desplegar.sh --compilar --datos-demo`;
  - configurar los secretos de GitHub (`PRODUCCION_*`) para que cada cambio a `main` se despliegue solo.
- **CI e integración:** no volver a fusionar con el CI en rojo, y proponer al equipo exigir el CI en `develop` y `main`. Confirmar el CI de `develop` en verde con las correcciones de Sebastián y llevar `develop` a `main`.
- **Próximos casos de uso:**
  - **CU-028**, permisos dinámicos: implementación acordada conmigo y pendiente según la guía del equipo.
  - **CU-006:** la liquidación al vendedor y la notificación siguen registrando lo que enviarían, sin abono real. Falta también el botón que aplique el tope de precio en el portal.
  - **CU-009:** registro de asistencia sin conexión en la app (cola local con clave de idempotencia).
  - **CU-010, paso 9:** aviso real a los asistentes; hoy es simulado y no hay canales push ni SMS.
  - **F14, con Diego:** avisos de logística sin destinatario filtrado.
- **Revisiones:** CU-019 con Diego, CU-021–023 con Daniel y CU-029 con Sebastián.
- **Entrega 2:** actualizar el SAD y los diagramas (siguen en ocho esquemas; hoy son once) para la Entrega 2 (20/11, tentativa).

---

## [12/11/2026]

**¿Qué hice?**
- **CU-028 · Gestión de roles y permisos.** Era el único caso de uso pendiente a mi nombre.
  - El administrador crea roles propios con una matriz de permisos por módulo y acción: eventos, personal, parqueaderos, emergencias y reportes. Los cuatro roles del sistema quedan fijos.
  - **CU-028B:** al restringir un permiso, la misma sesión pierde el acceso en su siguiente petición, sin volver a iniciar sesión. Identidad publica en Redis la matriz y los roles vigentes, y una guarda común del Núcleo los lee en cada petición. Esa guarda reemplazó las cuatro copias que tenía cada módulo.
  - **CU-028A:** un rol con usuarios activos solo se elimina reasignándolos a otro rol.
  - Control de versión entre administradores, auditoría de solo inserción y una migración nueva (36 migraciones, 87 tablas).
  - Pantalla nueva en el portal administrativo; una cuenta con un rol propio solo ve los módulos que puede leer.
  - Decisión registrada en `modulos/identidad/DECISIONES.md` §24. Descarté meter los permisos en el token (dura 15 min) y que el gateway le pregunte a Identidad en cada petición (es lo que quitó ADR-15).
- **F14:** los avisos de logística ya no se envían a la lista global. Cada empleado ve solo los suyos y quien supervisa ve todos. Lo hice yo en lugar de Diego.
- **Monitoreo:** Prometheus, Loki, Promtail y Grafana, con el tablero en `/grafana/` por el mismo gateway (`./iniciar.sh --monitoreo`).
  - Muestra CPU y memoria por instancia, peticiones por réplica, latencia y logs.
  - cAdvisor no funcionó con Docker Desktop: probé las versiones 0.49 y 0.52 y no ve los contenedores con el almacén de imágenes de containerd. Lo reemplacé con un exportador pequeño que lee la API de Docker y publica las mismas métricas.
- **Desempeño:** escribí `prueba-carga.py` para CU-006, CU-025 y CU-026.
  - Los tres cumplen p95 < 500 ms con 200 usuarios simultáneos, sin fallos.
  - El cuello de botella es el proceso Node de cada programa: llega a un núcleo completo, porque ejecuta la aplicación en un solo hilo.
  - Con 2 réplicas del Núcleo la capacidad subió 57 % (CU-026) y 82 % (CU-025).
  - Una primera conclusión mía culpaba a PostgreSQL y era falsa: venía de un error de medición de la CPU. Lo corregí y lo dejé escrito en la interpretación.
- **Disponibilidad:** `demo-disponibilidad.sh` escala Boletería a 3 réplicas o el Núcleo a 2 y tumba una con `kill -9` en medio del tráfico.
  - Ninguna de las cerca de 500 peticiones de esos segundos falló, en ningún caso.
  - Docker levantó la réplica en 8 a 13 s.
  - Probé el Núcleo con 2 réplicas: la demo completa de mis casos pasa contra él, así que se puede tumbar en vivo.
- **Demo de Playwright:** agregué el caso de CU-028 y una pausa de al menos 2 s por pantalla. Los 8 casos pasan; la demo dura unos 5 min 20 s.
- **Datos de Ventas borrados:** al correr `atributos-calidad.py` en mi entorno local se borraron las copias de Ventas de algunos eventos, y las compras que hubiera.
  - La causa es que la suite de consistencia vuelve a sembrar la base de Ventas.
  - Lo reparé reenviando los mensajes originales de CU-026.
  - Desde ahora esa suite solo corre con `--destructivas`.

## [13/11/2026]

**¿Qué hice?**
- **Cobertura al 100 %** en postventa (CU-006), personal-logística (CU-007 a CU-009), operación (CU-010), parqueaderos (CU-024, CU-025), eventos-recintos (CU-026), roles y permisos (CU-028) y la guarda común.
  - Encontré que la medición juntaba mal las pruebas unitarias con las e2e. Ahora `npm run test:cov:total` mide cada una con su herramienta y las une por línea.
  - Agregué una suite e2e de reventa en Boletería, más pruebas e2e y unitarias para las ramas que faltaban.
  - En total pasan 1049 unitarias, 132 e2e del Núcleo y 29 e2e de Boletería.
- Commit y push a `feature/samuel` ([`a7a135b`](https://github.com/Emperador24/HEXACORE/commit/a7a135bc91e15d9799ba34f8b0f0afbb0737ecd7), [`f2d96be`](https://github.com/Emperador24/HEXACORE/commit/f2d96be9fd2e803b4b9e232a921a6731c71c2314)), y PR [#51](https://github.com/Emperador24/HEXACORE/pull/51) hacia `develop`.

**Próximos pasos**
- Esperar el CI del PR #51 en verde antes de fusionar.
- Decidir con el equipo cuánto de la demo de Playwright se muestra en vivo: completa dura unos 5 min 20 s, y los 10 min son para los 32 casos.
- Ensayar el guion de `App/infra/DEMOSTRACION-ATRIBUTOS.md`: Grafana, prueba de carga rápida, caída de réplicas de Boletería y del Núcleo.
- Contarle a Diego cómo se mide ahora la cobertura (`test:cov:total`) y que F14 quedó resuelto.
- Avisar a Daniel que los consumidores de `eventos.gestion` en Ventas y Catálogo ya existen (los hice el 09/11) para que los revise.
- Pendientes de despliegue y de la Entrega 2: máquina de Oracle, SAD con once esquemas.

## [14/11/2026]

**¿Qué hice?**
- **Revisión contra lo que pide el profesor** para la sustentación y los entregables. Mis casos de uso y mis tres atributos están implementados y medidos. Lo que falta es documental:
  - En el SAD, la sección de tácticas y mediciones todavía tiene las cifras de la arquitectura ADR-12 (dice que no se han repetido) y no tiene sección de Monitoreo.
  - La presentación no tiene diapositivas de atributos, ni la de asignación por integrante, ni la comparación de contenedores antiguo vs. nuevo.
- **Demo de Playwright más corta:** cada pantalla se queda como mucho 1,5 s y `demo:ver` espera 300 ms entre acciones. Los 8 casos pasan de unos 5 min 20 s a unos 3 min 30 s. La versión corta (CU-010, CU-006 y CU-028) dura alrededor de 1,5 min.
  - Bajar solo la pausa casi no cambiaba nada: el tiempo se iba en la espera de 600 ms entre cada clic y cada tecleo.
- **Guía de demostración** (`App/frontend/demo-playwright/GUIA-DEMOSTRACION.md`): preparación del día anterior y de 15 minutos antes, comandos en vivo, qué decir en cada pantalla, plan B con los videos y problemas conocidos.
- **Error «Internal error: step id not found» en CU-028:** no era de la aplicación sino de Playwright 1.56.
  - Salía al cerrar la segunda ventana (la de la supervisora) sin cerrar primero su página, porque la captura final de cada caso buscaba esa página ya cerrada.
  - Lo comprobé apagando las capturas y el video por separado. Ahora se cierra la página antes que la ventana, y en tres corridas no volvió a salir.
- Commit y push a `feature/samuel` ([`5bb01a2`](https://github.com/Emperador24/HEXACORE/commit/5bb01a2a7cce6e5ea066873dfc62a4805f98ddb2)); entra en el PR [#51](https://github.com/Emperador24/HEXACORE/pull/51).

**Próximos pasos**
- Actualizar en el SAD mis tres atributos con las mediciones actuales y agregar la sección de Monitoreo.
- Hacer mis diapositivas: una por atributo y el despliegue con réplicas y monitoreo.
- Dejar el PR #51 en verde. El único trabajo que falla es la semilla de Alimentos, a la que le falta `cancelaciones_pedido` en el `TRUNCATE`; es de Sebastián y ya fallaba en el PR #49. Además el PR necesita la aprobación de un compañero.
- Acordar con el equipo qué casos se muestran en los 10 minutos de la demo y ensayar el guion de atributos.
