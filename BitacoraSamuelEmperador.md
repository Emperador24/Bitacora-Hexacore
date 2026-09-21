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
