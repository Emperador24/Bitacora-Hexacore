# Bitácora-Hexacore

Repositorio de bitácoras del equipo **Hexacore** para la asignatura de Arquitectura de Software.

## Objetivo

Las bitácoras son el registro trazable del trabajo del equipo a lo largo del proyecto. Sirven para:

- Dejar constancia de **qué se hizo, cuándo y quién lo hizo**, para que el avance del proyecto sea verificable en cualquier momento (por el equipo, el profesor o quien lo evalúe).
- Documentar el **razonamiento detrás de las decisiones** de arquitectura y de trabajo en equipo, no solo el resultado final.
- Facilitar el seguimiento individual del aporte de cada integrante.
- Servir de insumo para la evaluación del proceso, no solo del producto entregado.

## Estructura del repositorio

| Archivo | Contenido |
|---|---|
| `BitacoraGrupal.md` | Registro oficial de las reuniones del equipo: temas tratados, decisiones tomadas, acuerdos y tareas asignadas. |
| `BitacoraSamuelEmperador.md` | Bitácora personal de Samuel Emperador. |
| `BitacoraSebastianSanchez.md` | Bitácora personal de Sebastián Sánchez. |
| `BitacoraDiegoCoronado.md` | Bitácora personal de Diego Coronado. |
| `BitacoraDanielCristancho.md` | Bitácora personal de Daniel Cristancho. |
| `Cronograma.md` | Planificación semana a semana del proyecto (clases, entregables, trabajo interno) desde el 31 de julio hasta el 28 de noviembre de 2026. |

## Cronograma y fechas clave

Detalle completo, semana a semana, en [`Cronograma.md`](./Cronograma.md). Resumen de hitos:

| Hito | Fecha | Estado |
|---|---|---|
| Formación del equipo + 2 ideas de proyecto | 31 jul 2026 | ✅ hecho |
| Propuesta arquitectónica (QA priorizados, componentes, conexiones) | 18 ago 2026 | ✅ hecho |
| Diagramas C4 completos (6 diagramas + checklist) | 20 ago 2026 | ⚠️ en trabajo |
| Bitácora Arquitectónica creada (registro permanente) | 18 ago 2026 | ✅ en curso, continuo |
| Listado de casos de uso (25 CU, spreadsheet) | 20 ago 2026 | ✅ hecho |
| Utility Tree formal + tácticas de disponibilidad | 28 ago 2026 (tentativa) | ⬜ pendiente |
| Primer Parcial | 25 sep 2026 (tentativa) | ⬜ pendiente |
| **Entrega 1 (SAD v1, 15%)** | **9 oct 2026 (tentativa)** | ⬜ pendiente |
| Segundo Parcial | 6 nov 2026 (tentativa) | ⬜ pendiente |
| **Entrega 2 (prototipo + SAD v2, 25%)** | **20 nov 2026 (tentativa)** | ⬜ pendiente |
| Sustentaciones | 24–27 nov 2026 (tentativa) | ⬜ pendiente |
| Fin de semestre | **28 nov 2026 (confirmado)** | — |

> ⚠️ Las fechas marcadas **(tentativa)** son supuestos del equipo para poder planear (ver el aviso al inicio de `Cronograma.md`) y deben confirmarse con el profesor. Solo el **28 de noviembre de 2026** es una fecha dura conocida.

## Reglas y acuerdos del grupo de trabajo

### Reglas de las bitácoras

1. **Avance mínimo semanal (regla más importante).** Cada integrante debe registrar al menos **una entrada por semana** en su bitácora personal, sin excepción, aunque el avance de esa semana haya sido pequeño. Una semana sin entrada se interpreta como una semana sin trabajo.
2. **Todo debe corresponder con lo realmente realizado en el proyecto.** Las bitácoras no son de relleno: cada entrada debe reflejar trabajo verificable (commits, documentos, diseños, pruebas, etc.). No se registran tareas que no se hicieron ni se exagera el alcance de lo hecho.
3. **Las decisiones se registran donde se toman.** Toda decisión de arquitectura, alcance o forma de trabajo que afecte al equipo se documenta en `BitacoraGrupal.md`, en la sesión correspondiente, con su justificación y responsable — no solo el "qué" sino el "por qué".
4. **Fechas reales.** Cada entrada lleva la fecha en que ocurrió el trabajo o la reunión, no la fecha en que se escribió la bitácora.
5. **No se edita el pasado.** Si algo cambia respecto a lo registrado (una decisión se revierte, una tarea se reasigna), se documenta como una entrada nueva que referencia la anterior; no se borra ni se reescribe el historial.
6. **Trazabilidad con el trabajo técnico.** Cuando aplique, cada entrada debe referenciar el commit, PR, issue o documento asociado, para poder verificar el avance descrito.
7. **Claridad ante todo.** Se escribe para que cualquier integrante (o el profesor) entienda el avance sin tener que preguntar; se prefiere una entrada corta y clara sobre una larga y ambigua.
8. **Responsabilidad individual.** Cada integrante es responsable de mantener actualizada su propia bitácora personal. La bitácora grupal es responsabilidad compartida del equipo.

### Reunión de equipo

El grupo se reúne **todos los jueves a las 11:00 a.m., de forma presencial**. Cada reunión se registra como una sesión nueva en `BitacoraGrupal.md`.

## Cómo usar las plantillas

- Para una nueva reunión del equipo, duplica el último bloque `## Sesión N.º __` de `BitacoraGrupal.md`, numéralo y complétalo.
- Para un nuevo avance personal, duplica el último bloque de fecha `## [DD/MM/AAAA]` en tu bitácora personal y complétalo.
