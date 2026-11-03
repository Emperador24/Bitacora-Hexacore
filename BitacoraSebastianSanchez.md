# Bitácora Personal — Sebastián Sánchez

> Registro individual de trabajo. Bitácora del equipo: [BitacoraGrupal.md](./BitacoraGrupal.md)

## [04/08/2026]

### ¿Qué hice?
Hablé con mis compañeros sobre varias ideas que teníamos para el proyecto y al final decidimos trabajar con la idea de un centro de eventos.

### ¿Qué aprendí?
Pudimos aterrizar mejor qué queríamos hacer para el proyecto y escoger una idea entre las diferentes opciones que teníamos.

### Dificultades o dudas
Teníamos varias ideas y no estábamos seguros de cuál escoger.

### Próximos pasos
Empezar a definir mejor cómo va a funcionar el centro de eventos y qué cosas va a tener el sistema.


## [05/08/2026]

### ¿Qué hice?
Definí los casos de uso para la gestión de alimentación del centro de eventos. También estuvimos mirando si enfocarnos en el sistema de alimentación o en el de parqueaderos.

### ¿Qué aprendí?
Entendí mejor cómo plantear los casos de uso a partir de lo que necesita hacer el sistema.

### Dificultades o dudas
No estábamos seguros de si trabajar la parte de alimentación o la de parqueaderos.

### Próximos pasos
Terminar de organizar los casos de uso de alimentación y presentárselos al profesor.


## [06/08/2026]

### ¿Qué hice?
Le presentamos al profesor los casos de uso que habíamos definido para la gestión de alimentación.

### ¿Qué aprendí?
Con la retroalimentación del profesor vimos que el proyecto podía incluir más de un sistema y no teníamos que escoger solamente uno.

### Dificultades o dudas
Teníamos la duda de si debíamos quedarnos únicamente con alimentación o trabajar también otra parte del centro de eventos.

### Próximos pasos
El profesor nos indicó que agregáramos también el sistema de gestión de parqueaderos, así que el siguiente paso es definir sus casos de uso e integrarlos con los de alimentación.



## [10/08/2026]

### ¿Qué hice?
Terminé de definir bien los casos de uso que teníamos y los organicé en la plantilla de Excel, completando la información necesaria de cada uno.

### ¿Qué aprendí?
Aprendí a detallar mejor un caso de uso y a organizar toda su información dentro de la plantilla.

### Dificultades o dudas
Algunos casos de uso todavía necesitaban aterrizarse mejor para que quedara claro qué hacía cada uno.

### Próximos pasos
Revisar los casos de uso con el grupo y hacer los ajustes que sean necesarios antes de presentarlos.




## [13/08/2026]

### ¿Qué hice?
Revisamos con el profesor los casos de uso de gestión de alimentación y vimos que algunos se podían juntar porque hacían parte del mismo proceso. Por ejemplo, unimos "Gestionar preparación del pedido" con "Validar y entregar pedido". También agregué otros casos de uso para completar mejor la propuesta.

Además, con mi grupo empezamos a definir cómo íbamos a desarrollar el sistema. Decidimos hacer una aplicación móvil en Android Studio para los usuarios y una aplicación web para la parte administrativa.

En la aplicación móvil los usuarios podrán tener sus entradas a los eventos y utilizar los códigos QR necesarios para acceder y utilizar servicios como los parqueaderos. Por otro lado, la aplicación web estará enfocada en los administradores, para que puedan gestionar la información y las diferentes funcionalidades del sistema.

### ¿Qué aprendí?
Entendí mejor cómo separar las funcionalidades dependiendo del tipo de usuario. No todos necesitan utilizar la misma aplicación, ya que los usuarios necesitan principalmente acceder a sus entradas y servicios, mientras que los administradores necesitan herramientas para gestionar el sistema.

### Dificultades o dudas
Tuvimos que pensar cómo dividir las funcionalidades entre la aplicación móvil y la web, y cómo funcionaría el uso de los códigos QR para las entradas y los parqueaderos.

### Próximos pasos
Seguir definiendo las funcionalidades de la aplicación móvil y de la página web, y terminar de ajustar los casos de uso en la plantilla de Excel.


## [25/08/2026]

### ¿Qué hice?
Hablé con mi grupo sobre la arquitectura que podría tener el proyecto. Discutimos si para la compra de entradas íbamos a manejar timestamps o si era mejor trabajar solamente con una cola virtual. También evaluamos algunas opciones de bases de datos que podríamos utilizar para los diferentes componentes del sistema.

### ¿Qué aprendí?
Entendí que antes de definir la arquitectura hay que pensar bien cómo se van a manejar procesos importantes como la compra de entradas y qué base de datos se adapta mejor a cada necesidad.

### Dificultades o dudas
Todavía no teníamos claro si usar timestamps junto con la cola virtual o si la cola por sí sola era suficiente. También quedaron por revisar las opciones de bases de datos.

### Próximos pasos
Seguir evaluando estas alternativas y definir mejor la arquitectura que vamos a utilizar.



## [27/08/2026]

### ¿Qué hice?
Hablé con el profesor sobre las posibilidades que teníamos para el monitoreo del proyecto. Durante la conversación propuse utilizar Circuit Breaker como una posible opción, aunque quedó como algo tentativo mientras revisamos otras alternativas.

### ¿Qué aprendí?
Entendí mejor la importancia de pensar desde la arquitectura cómo vamos a monitorear el sistema y qué mecanismos podemos usar para detectar o manejar problemas.

### Dificultades o dudas
Todavía no está definido qué mecanismo vamos a utilizar para el monitoreo. Circuit Breaker es una posibilidad, pero tenemos que revisar otras opciones antes de decidir.

### Próximos pasos
Investigar otras alternativas de monitoreo y compararlas con Circuit Breaker para decidir cuál tiene más sentido para el proyecto.


## [19/09/2026]

> Registro retrospectivo agregado el 22/09/2026. La fecha del encabezado corresponde a los commits, en UTC−05:00; esta entrada no fue escrita ese día. Los aprendizajes y próximos pasos se reconstruyen al revisar los cambios.

### ¿Qué hice?
Creé la estructura base del servicio de Pedidos con NestJS, su configuración, las variables de entorno y el Dockerfile. También incorporé los cambios de develop a mi rama feature/sebastian.

Como contexto personal, antes de comenzar la implementación estuve revisando y entendiendo el proyecto y su arquitectura. Esa preparación previa no tiene evidencia individual fechada en Git, por lo que la consolido en esta entrada sin asignarle una fecha propia.

### ¿Qué aprendí?
Al revisar este trabajo, destaco cómo se organiza un servicio separado y cómo se prepara su configuración para conectarlo con la base de datos, Redis, RabbitMQ y la pasarela de pagos.

### Dificultades o dudas
La estructura inicial todavía no implementaba la lógica de pedidos. Quedaba por desarrollar la persistencia y conectar las funciones del servicio.

### Próximos pasos
A partir de lo que había en este punto, seguía configurar la persistencia y modelar el catálogo, los pedidos y sus transacciones de pago.

### Evidencia

- [`5a6bb66`](https://github.com/Emperador24/HEXACORE/commit/5a6bb66fdc12929268c4f5959a72c162bfb8c1bb) — Estructura base del servicio de Pedidos
- [`01e1087`](https://github.com/Emperador24/HEXACORE/commit/01e1087aa0a8a50faf492d08f81f906d19fed028) — Merge branch 'develop' into feature/sebastian
- [`059d1f3`](https://github.com/Emperador24/HEXACORE/commit/059d1f34d6448ed3629848a40a882a5349f4c3f2) — Merge remote-tracking branch 'origin/develop' into feature/sebastian


## [20/09/2026]

> Registro retrospectivo agregado el 22/09/2026. La fecha del encabezado corresponde a los commits, en UTC−05:00; esta entrada no fue escrita ese día. Los aprendizajes y próximos pasos se reconstruyen al revisar los cambios.

### ¿Qué hice?
Configuré la persistencia del servicio de Pedidos y modelé los establecimientos, los productos, los pedidos, sus detalles y las transacciones de pago. Agregué las migraciones y los datos de ejemplo.

También implementé las consultas del catálogo, la autenticación y una primera versión del checkout para crear pedidos pendientes de pago. Agregué pruebas para la autenticación y el checkout.

### ¿Qué aprendí?
Al revisar estos cambios, destaco la importancia de separar el pedido, sus productos y los intentos de pago. También queda clara la diferencia entre consultar si hay inventario y reservarlo para una compra.

### Dificultades o dudas
El checkout inicial validaba las existencias, pero todavía no reservaba inventario. Además, su duración de diez minutos quedó indicada en el código como una decisión temporal porque CU-011D no fijaba ese tiempo.

### Próximos pasos
A partir de esta versión, seguía implementar los pagos y conectar el checkout con las reservas de inventario.

### Evidencia

- [`9582d3e`](https://github.com/Emperador24/HEXACORE/commit/9582d3e51765e6239c4a460b9f1b3016754a5665) — Configura persistencia base del servicio de Pedidos
- [`b0e9221`](https://github.com/Emperador24/HEXACORE/commit/b0e9221a0f369de1df2f1264221354d881d4ac1f) — Modela catalogo e inventario base de Pedidos
- [`5c7ed5d`](https://github.com/Emperador24/HEXACORE/commit/5c7ed5dedb606cc8e5d6d66482c29b0f9512f567) — Modela pedidos y detalles de pedido
- [`e8a0bce`](https://github.com/Emperador24/HEXACORE/commit/e8a0bceb0a0f91655041f6be08d0ab686f4c18ac) — Registra transacciones de pago de pedidos
- [`89ecb19`](https://github.com/Emperador24/HEXACORE/commit/89ecb193ee36dd46b7aa807adc3ad5a374ed9181) — Configura migraciones y semillas de Pedidos
- [`82f5163`](https://github.com/Emperador24/HEXACORE/commit/82f5163ac8236aa07c86e8849160e6be2ad761df) — Implementa consultas de catalogo para Pedidos
- [`8ed65c0`](https://github.com/Emperador24/HEXACORE/commit/8ed65c051cfaaae7c7f4a885fc2bedb379466331) — Integra autenticacion al servicio de Pedidos
- [`62533e4`](https://github.com/Emperador24/HEXACORE/commit/62533e488714f3b0a053ac88bc4393ad4fc58fad) — Implementa checkout inicial de Pedidos


## [21/09/2026]

> Registro retrospectivo agregado el 22/09/2026. La fecha del encabezado corresponde a los commits, en UTC−05:00; esta entrada no fue escrita ese día. Los aprendizajes y próximos pasos se reconstruyen al revisar los cambios.

### ¿Qué hice?
Implementé los pagos y las reservas de inventario con Redis, incluida su preparación y la conexión con el checkout. Agregué la confirmación del pedido después de un pago aprobado, la generación del código QR, la publicación de pedidos confirmados mediante RabbitMQ y la liberación de inventario cuando vence el checkout.

Integré el servicio con Docker y el API Gateway. También incorporé cambios de develop a mi rama, conecté el flujo de pedidos CU-011 en la web y en la aplicación móvil, y mejoré la presentación web y los datos de ejemplo.

Agregué pruebas E2E del servicio con PostgreSQL, Redis, RabbitMQ y la pasarela simulada en Docker. El commit respalda la incorporación de esas pruebas; no es un registro de sus resultados de ejecución.

### ¿Qué aprendí?
Al revisar este trabajo, destaco que confirmar un pago requiere coordinar el estado del pedido y el inventario, y evitar que un reintento vuelva a cobrar o descontar productos. Las pruebas incorporadas permiten revisar ese flujo junto con el QR y el mensaje del pedido confirmado.

### Dificultades o dudas
La preparación del inventario en Redis requería detener las compras y comprobar que no hubiera reservas o pagos pendientes. También había que contemplar pagos con resultado incierto y evitar liberar una reserva mientras el pago seguía sin resolverse.

### Próximos pasos
A partir del estado alcanzado, seguía integrar los pedidos confirmados en la vista del restaurante y continuar con la administración de disponibilidad del menú. Esos cambios aparecen en commits del 22 de septiembre y quedan fuera de este registro.

### Evidencia

- [`fc6080a`](https://github.com/Emperador24/HEXACORE/commit/fc6080aa54f85be5e9017a337fe05301e7dde6bd) — Implementa pagos de Pedidos
- [`57f6baf`](https://github.com/Emperador24/HEXACORE/commit/57f6baf170c468057d794ea7b234bb36e639c942) — Merge remote-tracking branch 'origin/develop' into feature/sebastian
- [`d73115e`](https://github.com/Emperador24/HEXACORE/commit/d73115eb8a8505dda6324893cf674972dad1f1f2) — Implementa reservas atomicas de inventario con Redis
- [`723a749`](https://github.com/Emperador24/HEXACORE/commit/723a7496eb64c5abd4cc8a4a3e33ad5b9db74cec) — Prepara inventario Redis de forma segura
- [`08db928`](https://github.com/Emperador24/HEXACORE/commit/08db928700b2e86b0eb46da4253ba42ad301d3b3) — Integra reserva de inventario con checkout
- [`644598f`](https://github.com/Emperador24/HEXACORE/commit/644598f57f77eebe5a90b25385eec0be34074ca1) — Finaliza pedidos tras pago aprobado
- [`5263abe`](https://github.com/Emperador24/HEXACORE/commit/5263abeae2715d413f15041268d3fa670ace2b26) — Genera QR al confirmar pedidos
- [`1533df7`](https://github.com/Emperador24/HEXACORE/commit/1533df735d041011ad8045b888d2dccbd4c224d5) — Publica pedidos confirmados mediante RabbitMQ
- [`00efd7e`](https://github.com/Emperador24/HEXACORE/commit/00efd7ec669591388b3740809b968a579adce13d) — Expira checkouts y libera inventario reservado
- [`714f426`](https://github.com/Emperador24/HEXACORE/commit/714f42636b543a856b979cea89025261e24eeeb3) — Integra servicio de pedidos con Docker y API Gateway
- [`c093c4c`](https://github.com/Emperador24/HEXACORE/commit/c093c4c311be528b95b87f8a840d1366f51a34eb) — Integra flujo web de pedidos CU-011
- [`7ddde8d`](https://github.com/Emperador24/HEXACORE/commit/7ddde8d9d7113d08183981a83cdb07604a2282af) — Mejora experiencia web y datos demo de pedidos
- [`5f92b3a`](https://github.com/Emperador24/HEXACORE/commit/5f92b3a5890578b4b83e8993a1697612e9b5f96a) — Implementa flujo movil de pedidos CU-011
- [`4417fdb`](https://github.com/Emperador24/HEXACORE/commit/4417fdba5512a0549acd39955e93e706994124b0) — Agrega pruebas E2E reales para CU-011


## [22/09/2026]

> Registro retrospectivo agregado el 22/09/2026, después de los cambios descritos. La fecha del encabezado corresponde a los commits, en UTC−05:00. Los aprendizajes y próximos pasos se reconstruyen al revisar los cambios.

### ¿Qué hice?
Integré los pedidos confirmados en la vista del restaurante de la aplicación móvil. Agregué la consulta en el servicio de Pedidos para mostrar los productos, las cantidades y el total de cada pedido confirmado del establecimiento.

También implementé la administración básica de disponibilidad del menú CU-012, con una pantalla para activar o desactivar productos y su conexión con el backend. Agregué pruebas del servicio y de las pantallas móviles para estos cambios, e incorporé los cambios de develop a mi rama feature/sebastian.

### ¿Qué aprendí?
Al revisar estos cambios, destaco la diferencia entre consultar los pedidos confirmados y gestionar su preparación o entrega. También queda clara la importancia de actualizar solamente la disponibilidad de un producto para no sobrescribir su precio o inventario.

### Dificultades o dudas
La vista de pedidos todavía era de consulta y no gestionaba la preparación ni la entrega. En el menú había que manejar los errores de conexión sin mostrar como confirmado un cambio cuya respuesta no se había recibido.

### Próximos pasos
A partir de esta versión, queda revisar el flujo de consulta y disponibilidad con las pruebas incorporadas, y continuar con la gestión de preparación y entrega que todavía no cubre la vista del restaurante. Los commits registran la incorporación de pruebas, pero no sus resultados de ejecución.

### Evidencia

- [`d5e9ef5`](https://github.com/Emperador24/HEXACORE/commit/d5e9ef5cbf2aac3816bc1f4029c32a09b93f23e0) — Integra pedidos confirmados en vista de restaurante
- [`89b9fb1`](https://github.com/Emperador24/HEXACORE/commit/89b9fb1c5f6893645469da449d9f427bff9d3a7c) — Merge remote-tracking branch 'origin/develop' into feature/sebastian
- [`f6c18f3`](https://github.com/Emperador24/HEXACORE/commit/f6c18f3027fa169e7fde0706c5329e55b183d919) — Implementa administracion de disponibilidad del menu CU-012


## [01/11/2026]

> Entrada agregada el 02/11/2026 para registrar el trabajo del domingo. Las fechas de los commits están en hora de Bogotá (UTC−05:00). Corresponde a la semana del 26 de octubre al 1 de noviembre.

### ¿Qué hice?
Revisé el proyecto y los cambios de arquitectura con ayuda de Codex. Organicé un plan para juntar varias partes del backend y hacer más sencillo el programa, manteniendo lo que ya estaba hecho y dejando los casos de uso que faltan para cada compañero.

Empecé arreglando la configuración de Docker para el modo remoto y recuperando las pruebas de compra de alimentos. Después reuní Identidad y Alimentos en el Núcleo y agregué Personal/Logística. Dejé sus bases separadas por el momento para comprobar primero que todo siguiera funcionando al mover el código.

También preparé las pruebas de referencia de Boletería para comparar cómo funcionaba antes de juntarla. Ese domingo quedó lista la referencia; el traslado de Boletería se publicó el lunes.

### ¿Qué aprendí?
Entendí mejor que un módulo no tiene que ser otro servicio separado. Varias partes del sistema pueden funcionar dentro del mismo programa y seguir organizadas en sus propios módulos.

También me quedó más claro por qué conviene probar lo que hay antes de moverlo: así podemos distinguir un problema que ya existía de uno causado por la migración.

### Dificultades o dudas
Encontré pruebas que estaban mal conectadas a sus dependencias y otras que podían terminar sin comprobar nada si Redis no respondía. Hubo que revisar eso y resolver problemas al cargar NestJS desde las pruebas.

Juntar el código tampoco solucionaba automáticamente los problemas de datos. Por ejemplo, el QR podía tardar en actualizarse y eso tenía que quedar documentado.

### Próximos pasos
Seguir con Boletería, pasar Pagos a un módulo compartido, mover el correo al Trabajador y después revisar cómo juntar las bases de datos sin perder información.

### Evidencia

5 commits del domingo, de la semana del 26/10 al 01/11:

- [`c6c6e92`](https://github.com/Emperador24/HEXACORE/commit/c6c6e9223a811bf2d3acca999b49436236bd7cef) — fix(infra): reparar Compose remoto y registrar plan de migración (18:56, hora de Bogotá).
- [`25a4fd3`](https://github.com/Emperador24/HEXACORE/commit/25a4fd3a98e3ba69ae8642d53253720f73e0621a) — test(alimentos): recuperar integración aislada de CU-011 (19:59, hora de Bogotá).
- [`8fff023`](https://github.com/Emperador24/HEXACORE/commit/8fff023cf5b5b8ce88e5e279e75165c46dfc8fa9) — refactor(backend): integrar identidad y alimentos en nucleo modular (21:05, hora de Bogotá).
- [`125fe36`](https://github.com/Emperador24/HEXACORE/commit/125fe36d874efc0f30d268a3219635854b807b82) — refactor(backend): incorporar personal y logistica al nucleo (22:56, hora de Bogotá).
- [`d48beff`](https://github.com/Emperador24/HEXACORE/commit/d48befff29244bdd2746ba4686c519c13a28cc4c) — test(boleteria): establecer integracion aislada antes del traslado (23:25, hora de Bogotá).


## [02/11/2026]

> Entrada agregada después de los cambios descritos. Las fechas están en hora de Bogotá (UTC−05:00). Corresponde a la semana del 2 al 8 de noviembre.

### ¿Qué hice?
Seguí la migración con ayuda de Codex. Junté Ventas, Catálogo, Fila, Postventa y Acceso QR en Boletería. También pasé Pagos a un módulo que pueden usar Núcleo y Boletería, quité las llamadas HTTP internas hacia el servidor anterior y dejé un solo receptor del webhook en el Núcleo.

Moví el envío de correos que ya existía al Trabajador. Después preparé una copia de las ocho bases y probé cómo pasarlas a una sola base con ocho esquemas. Revisé que se conservaran los registros, los pagos y los historiales. También se probaron los respaldos y su restauración.

Con ese ensayo listo, adapté las aplicaciones para usar la base común. Probé una copia con datos transferidos y una instalación nueva, y dejé la preparación de las migraciones en una tarea que corre antes de arrancar las aplicaciones.

Actualicé la documentación, los diagramas y las guías para el equipo. Dejé el PR #44 en borrador y se ejecutaron las pruebas remotas y la publicación de imágenes. Hubo que corregir problemas de preparación del pipeline y cambiar la compilación de las dos plataformas a ejecutores nativos.

Por último dejé un entorno de revisión que se construye desde mi rama, con los dos portales y cuentas de prueba. Se comprobó que se puede entrar, hacer los recorridos implementados y reiniciar conservando los datos. Todo quedó publicado en `feature/sebastian-arquitectura`, sin mezclarlo con `develop` ni con `main`.

### ¿Qué aprendí?
Me quedó más clara la diferencia entre juntar programas y juntar bases de datos. Aunque las tablas estén en una sola base, hay que seguir teniendo claro qué módulo maneja cada dato.

También entendí que revisar solamente cuántas filas se copiaron no basta: hay que comprobar su contenido, las referencias, los valores de los pagos y los historiales. Y volver a una imagen vieja no significa que los datos o los cobros vuelvan al estado anterior.

### Dificultades o dudas
Había tablas y secuencias con nombres repetidos entre las bases. También tuve que conservar las migraciones anteriores y revisar que cada parte buscara sus tablas en el esquema correcto.

Se presentaron fallos en algunas pruebas y en la construcción de imágenes; los intentos y sus correcciones quedaron registrados. Además siguen pendientes problemas previos de pagos inciertos, timeouts, notificaciones de logística y correo, identificados como F12/F13/F14/F15. Los casos de uso que todavía faltan siguen con sus responsables.

### Próximos pasos
Probar la rama con otro compañero, anotar lo que encontremos y corregir los problemas de la migración que aparezcan. Después de esa revisión decidiremos cuándo integrar los cambios. La instalación habitual anterior sigue sin modificarse.

### Evidencia

14 commits del lunes, de la semana del 02/11 al 08/11:

- [`e08daf6`](https://github.com/Emperador24/HEXACORE/commit/e08daf68e204e8fa43d04ad40ce3a3f11a2060bf) — refactor(backend): integrar componentes de boleteria en una aplicacion (03:43, hora de Bogotá).
- [`f070bc2`](https://github.com/Emperador24/HEXACORE/commit/f070bc2fe6f691741623ee93b4041765100b1c69) — refactor(pagos): extraer modulo reutilizable conservando interfaz HTTP (05:38, hora de Bogotá).
- [`85419be`](https://github.com/Emperador24/HEXACORE/commit/85419bef9d2c88cd27301923e7e8252fbc75e863) — refactor(pagos): integrar llamadas locales y retirar servidor HTTP (09:36, hora de Bogotá).
- [`300a88e`](https://github.com/Emperador24/HEXACORE/commit/300a88ebd4337bb4538d9229c84af0361a6afd9f) — refactor(backend): trasladar notificaciones al trabajador (11:02, hora de Bogotá).
- [`be57961`](https://github.com/Emperador24/HEXACORE/commit/be57961472a0802c90a57d247fb67e96e6717b1b) — feat(datos): preparar y verificar consolidacion aislada por esquemas (13:19, hora de Bogotá).
- [`6e2260a`](https://github.com/Emperador24/HEXACORE/commit/6e2260a31651760f5867e7c3e0f121fbcc0f802f) — refactor(datos): conectar aplicaciones a base unica por esquemas (15:55, hora de Bogotá).
- [`58b8326`](https://github.com/Emperador24/HEXACORE/commit/58b832625e8a52a7798e2c68241a3e155174fdd3) — ci: verificar migracion y publicar arquitectura por digest (16:28, hora de Bogotá).
- [`7b34b71`](https://github.com/Emperador24/HEXACORE/commit/7b34b71f72c65174cc154cfa3c39ce1a7aab9295) — fix(ci): adaptar referencia historica y salud conjunta del nucleo (16:37, hora de Bogotá).
- [`82c5218`](https://github.com/Emperador24/HEXACORE/commit/82c52188d441edc05d2488fd04de42abc272c958) — docs(arquitectura): registrar ADR-16 y preparar revision del equipo (16:37, hora de Bogotá).
- [`36090b3`](https://github.com/Emperador24/HEXACORE/commit/36090b3b5a3591953fe32dfde231f21c01fbb06c) — fix(test): conservar digests publicados durante reinicio financiero (17:25, hora de Bogotá).
- [`c36427a`](https://github.com/Emperador24/HEXACORE/commit/c36427ac7b217cdb3a37c8a75b545d0fe9aef5d9) — fix(cd): compilar plataformas nativas y verificar sus manifiestos (17:45, hora de Bogotá).
- [`5183bc3`](https://github.com/Emperador24/HEXACORE/commit/5183bc3c418702514e3c2b4bc5f2d8a7b3aa9270) — docs(migracion): registrar verificacion remota y cierre tecnico (18:01, hora de Bogotá).
- [`9acfb65`](https://github.com/Emperador24/HEXACORE/commit/9acfb652e8fd4745b6eb2e36627caa9a32924500) — feat(dev): preparar entorno de revision de arquitectura (18:59, hora de Bogotá).
- [`6ce7f8b`](https://github.com/Emperador24/HEXACORE/commit/6ce7f8b7a391870d8123ff1bed2f3c22f34fa916) — fix(dev): esperar la preparacion finita antes de iniciar aplicaciones (19:02, hora de Bogotá).

El último commit aparece el 03/11 en UTC, pero en Bogotá corresponde al lunes 02/11 a las 19:02. Entre ambos días son 19 commits de migración.

- [PR #44 en borrador](https://github.com/Emperador24/HEXACORE/pull/44).
- [Pruebas remotas aprobadas sobre 6ce7f8b](https://github.com/Emperador24/HEXACORE/actions/runs/41549909189).
- [Publicación y comprobación de imágenes de c36427a](https://github.com/Emperador24/HEXACORE/actions/runs/41541166454).
- [Registro técnico de las etapas y resultados](https://github.com/Emperador24/HEXACORE/blob/6ce7f8b7a391870d8123ff1bed2f3c22f34fa916/Documentation/Work/ESTADO-MIGRACION.md).
- [Guía para arrancar y probar la rama](https://github.com/Emperador24/HEXACORE/blob/6ce7f8b7a391870d8123ff1bed2f3c22f34fa916/App/infra/revision/README.md).
