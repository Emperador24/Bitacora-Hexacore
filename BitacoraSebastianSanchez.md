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
