# Bitácora Personal — Diego Coronado
> Registro individual de trabajo. Bitácora del equipo: [BitacoraGrupal.md](./BitacoraGrupal.md)

## [13/08/2026]
**¿Qué hice?**
- Desarrollé los CU-LOG-001 – CU-LOG-005 (Logística y Operación del Evento: planificar logística, asignar personal operativo, gestionar turno y asistencia del personal, monitorear el evento, gestionar incidentes) y los CU-PARK-001 – CU-PARK-005 (Parqueadero: reservar parqueadero, ingreso y salida de vehículos, asignación de espacios, cobro, control de ocupación).
- Fusioné los casos de uso de "Gestionar Cambios de Turno" y "Registrar Ingreso y Salida del Personal" en uno solo (CU-LOG-003), al identificar que ambos describían acciones sobre el mismo actor (personal operativo) dentro del mismo flujo operativo.

**¿Qué aprendí?**
- A aplicar la plantilla estándar de casos de uso (Objetivo en Contexto, Actores, Pre/Post-condiciones, Flujo Actor/Sistema paso a paso, Flujos alternativos, Caminos de Excepción) y a decidir cuándo dos casos de uso deben unirse en vez de mantenerse separados, para evitar fragmentar procesos que en realidad comparten actor y objetivo.

**Dificultades o dudas**
- Definir si el control de ocupación de Parqueadero debe alimentarse de los mismos indicadores que usa Logística para el monitoreo del evento, o si debe ser independiente.

**Próximos pasos**
- Revisar con el equipo la numeración final de los CU antes de consolidar el documento completo.

---

## [27/08/2026]
**¿Qué hice?**
- Cerré los pendientes que quedaban abiertos en la v1.0 del SAD (DescripcionArquitecturaSoftware.tex): subí la versión a 1.1 y actualicé la fecha de entrega.
- Dibujé el diagrama de clases UML del modelo de dominio en TikZ (18 clases con sus relaciones y multiplicidades).
- Documenté los componentes internos de los servicios de Personal, Eventos/Emergencias y Parqueaderos (antes solo estaba detallado el de Entradas/Mercado Secundario).
- Describí los ambientes de desarrollo y pruebas en la vista física (topología reducida de producción, CI en dev, pruebas de carga en test).
- Detallé el modelo de datos por microservicio, con esquemas y llaves foráneas lógicas.
- Corregí una referencia rota a la tabla del modelo de dominio.

**¿Qué aprendí?**
- Con base de datos independiente por microservicio (ADR-01) las referencias entre dominios no pueden ser llaves foráneas físicas, porque cada esquema vive en su propia base; toca resolverlas a nivel de aplicación guardando el id y validando desde el servicio dueño del dato.

**Dificultades o dudas**
- Qué tan detallado dejar el diagrama de clases en esta versión (simplificado, con multiplicidades) sin meterme ya en navegabilidad y tipos de dato exactos, que dependen de decisiones que aún no están cerradas.

**Próximos pasos**
- Refinar el modelo entidad-relación de cada microservicio junto con el prototipo funcional y definir el motor de base de datos concreto por dominio.

---

## [06/09/2026]
**¿Qué hice?**
- Migré toda la app de Kotlin a Flutter y la reimplementé desde cero (hexacore_cliente pasó a llamarse hexacore_app: pubspec.yaml, bundle ID iOS, applicationId/namespace Android, MainActivity, Info.plist).
- Arreglé el debugging inalámbrico en iOS (era permisos de Automatización de Xcode y Red Local); por USB sí funcionaba.
- Rediseñé las 16 pantallas con estilo Liquid Glass (iOS 26): fondo oscuro, blobs difuminados, vidrio de verdad con BackdropFilter, tipografía Space Grotesk/Manrope, badges por categoría y nav flotante tipo pill. Primero hice un mockup para validar el estilo porque el primer intento quedó muy tibio.
- Dejé corriendo un build release para no depender del cable/Mac para probar.
- Hice el flujo de registro: Google/Apple simulados, registro por correo o teléfono, OTP de 6 dígitos (código de prueba 123456) con contador de reenvío.
- Terminé compra de entradas (checkout) y búsqueda/filtro de eventos por categoría.
- Implementé reventa de entradas (mercado secundario).
- Agregué notificaciones (turnos, incidentes, emergencias).
- Puse ícono de app y splash screen propios.
- Implementé recuperar contraseña.

**¿Qué aprendí?**
- Migrar de Kotlin a Flutter me obligó a repensar la arquitectura completa: en Kotlin el layout era todo XML + Views, y en Flutter es composición de widgets, así que terminé reorganizando la app por componentes reutilizables en vez de una pantalla por archivo.
- Para el efecto Liquid Glass entendí bien cómo funciona BackdropFilter (blur real sobre lo que hay detrás) combinado con opacidad y bordes, algo que en Kotlin nativo hubiera sido mucho más complicado de lograr.

**Dificultades o dudas**
- Google/Apple Sign-In quedan simulados por ahora porque no hay backend ni credenciales reales (Apple Developer de pago, Client ID de Google).

**Próximos pasos**
- Correcciones de frontend y backend completo.

---

## [13/09/2026]

**¿Qué hice?**
- Corregí el PR #10 (feature/diego → main), que debía apuntar a develop — quedó feature/diego → develop, mergeable sin conflictos.
- Confirmé mi alcance real revisando el README del SAD: App/services/eventos-emergencias, CU-016 a CU-020 (logística). Los de parqueadero no son míos, son de Daniel y Samuel.
- Elegí CU-018 (Gestionar turno y asistencia del personal) como mi caso de uso complejo, siguiendo el criterio real del equipo: no el flujo más largo, sino el que ya tiene infraestructura no trivial documentada (offline-first + cola de mensajes) en CU_eventos_completo.xlsx.
- Construí el backend real desde cero: NestJS + TypeORM + PostgreSQL. Entidades (Empleado, Turno, SolicitudCambioTurno, RegistroAsistencia), lógica de solicitud/aprobación de cambio de turno con validación de horas máximas y búsqueda automática de reemplazo, y registro de entrada/salida con detección de credencial inválida, turno no vigente y duplicados.
- Agregué la infraestructura no trivial que exige la ficha del CU: cola de mensajes RabbitMQ (Publicador/Consumidor de Eventos) para propagar cambios de turno aprobados, y soporte offline-first (idempotencyKey + timestamp del cliente) en el registro de asistencia.
- Instalé Docker, levanté PostgreSQL y RabbitMQ reales, y verifiqué todo el flujo end-to-end.
- Escribí 20 pruebas de integración contra la infraestructura real; llegué a 97.7% de cobertura.

**¿Qué aprendí?**
- A elegir el caso de uso complejo con criterio de arquitectura (infraestructura no trivial demostrable), no por instinto de "cuál se ve más largo".
- Un gotcha real de TypeORM: si cargas una relación eager y luego reasignas solo la FK cruda (turno.empleadoId = x), el save() la revierte silenciosamente porque prioriza el objeto de la relación — hay que reasignar ambos.
- Con ESM real (nodenext), una referencia circular entre dos entidades que se necesitan mutuamente revienta en producción aunque los tests con vitest la toleren — se soluciona con el tipo Relation<T> de TypeORM.

**Dificultades o dudas**
- Encontré varios bugs solo al probar contra infraestructura real que los tests con mocks nunca hubieran detectado (columnas nullable sin tipo explícito, la relación stale ya mencionada).

**Próximos pasos**
- Conectar la GUI de Flutter a este backend real y probarlo de punta a punta en el navegador.

---

## [14/09/2026]

**¿Qué hice?**
- Conecté ShiftsPage, AttendancePage y RequestsReviewPage de la app Flutter al backend real (antes eran 100% mock). Probé el flujo completo en Chrome: login → ver turno real → solicitar cambio → jefe de personal aprueba → turno se reasigna de verdad en la base de datos → registrar entrada/salida de asistencia.
- Intenté desplegar en mi iPhone físico. Falló por un bug de macOS (com.apple.provenance bloqueando el firmado de código del framework de Flutter) — diagnostiqué la causa raíz hasta el fondo, pero lo dejé pendiente porque requiere sudo y no era bloqueante para demostrar el trabajo (Chrome ya prueba el flujo completo).
- Descubrí que tenía dos clones locales del repo desincronizados (~/HEXACORE, donde tengo VS Code abierto, y otra copia donde había estado trabajando) — sincronicé todo el trabajo de esta semana a la carpeta correcta y quedó comiteado ahí.
- Hice commit de todo el trabajo (backend + GUI conectada) en feature/diego y lo subí a origin/feature/diego.
- Revisé el estado general de la entrega contra la rúbrica de la primera entrega: identifiqué qué me falta a mí (bitácora al día, prepararme para las preguntas de "conocimiento de lo entregado") y qué falta a nivel de equipo (SRS formal, diapositivas, CI/CD, desplegabilidad en 2+ computadoras — nada de eso existe todavía en el repo).

**¿Qué aprendí?**
- A no dar nada por hecho con las rutas de trabajo: tener dos clones del mismo repo en carpetas distintas genera confusión real sobre "dónde están mis cambios" si no se verifica con cuidado.

**Dificultades o dudas**
- El despliegue a dispositivos físicos iOS sigue bloqueado por el bug de macOS; falta resolverlo si quiero demostrarlo en el celular real el día de la sustentación.

**Próximos pasos**
- Coordinar con el equipo lo pendiente grupal (CI/CD, desplegabilidad, diapositivas, SRS) — no es algo que pueda resolver solo.
- Repasar el código a fondo para las preguntas de "conocimiento de lo entregado" (25% del total).

---
