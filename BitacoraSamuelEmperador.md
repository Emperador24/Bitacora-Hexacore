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
