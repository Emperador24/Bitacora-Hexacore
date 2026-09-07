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
