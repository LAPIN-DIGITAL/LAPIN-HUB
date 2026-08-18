> **Versión:** 2.1
> **Fecha:** 18/08/2026
> **Autor:** Jessica

# Estructura y configuración del sistema de gestión

## Propósito

Definir el modelo estándar que LAPIN DIGITAL utiliza para organizar, visualizar y registrar su trabajo — independientemente de la herramienta que lo implemente.

Este documento no explica cómo funciona una herramienta particular. Documenta cómo LAPIN necesita que funcione su sistema de gestión.

---

## 1. Modelo vs. herramienta

LAPIN separa el **modelo de gestión** (cómo representamos el trabajo) de la **herramienta** (qué producto lo implementa). Hoy es GitHub Projects; mañana puede ser otra cosa. El modelo debe sobrevivir a ese cambio.

Esto define tres niveles:

- **Necesidad** — qué problema resolvemos y qué debe poder hacer una herramienta.
- **Modelo de gestión** — cómo representamos el trabajo (los parámetros de la sección 3), sin importar el producto.
- **Herramienta** — la implementación concreta del modelo.

El flujo de decisión es siempre:

**Necesidad → Criterios de evaluación → Selección de herramienta → Configuración según el modelo LAPIN**

Nunca al revés: no adoptamos primero una herramienta y modificamos el modelo para adaptarnos a sus límites. Si una herramienta no puede representar un parámetro que consideramos fundamental, eso ya es una señal de que no sirve.

---

## 2. Principio de simplicidad

El sistema registra lo que resulta útil para gestionar, medir o reconstruir el trabajo. No se incorporan campos, estados, clasificaciones, vistas, relaciones o automatizaciones solo porque la herramienta lo permita — cada elemento debe responder a una necesidad concreta.

Tampoco se registra cada acción realizada. Crear un campo, ajustar un color o ejecutar un paso menor puede formar parte de una actividad sin necesitar una unidad de trabajo independiente.

> Mantener el sistema no debe convertirse en el trabajo.

---

## 3. Parámetros del modelo

Estos son los parámetros que cualquier herramienta debe poder representar (o un concepto equivalente). La columna derecha muestra cómo están implementados hoy en GitHub Projects.

| Parámetro | Qué representa | Implementación actual (GitHub) |
|---|---|---|
| **Work Item Type** | Qué tipo de unidad de trabajo es (ver sección 4) | Campo estructurado: `EPIC`, `USER STORY`, `TASK`, `BUG` |
| **Rol responsable** | Qué Rol de LAPIN tiene la responsabilidad funcional | Campo personalizado con los Roles definidos por LAPIN |
| **Activity Type** | Qué naturaleza tiene el trabajo (ver sección 6) | Campo personalizado de selección única |
| **Status** | En qué situación se encuentra | Campo de estado (columnas del Board) |
| **Priority** | Qué nivel de prioridad tiene | Campo personalizado |
| **Iteration** | A qué período de trabajo pertenece | Campo de iteración |
| **Estimate** | Tamaño relativo (Story Points) | Campo numérico: `1, 2, 3, 5, 8, 13` |
| **Created / Updated** | Cuándo se creó / actualizó | Automático (GitHub) |
| **Start Date / Due Date / Finish Date** | Cuándo empezó / debía terminar / terminó realmente | Campos de fecha |
| **Labels** | Clasificación complementaria | Labels de GitHub |
| **Parent / jerarquía** | Relación con una unidad superior | Parent / Sub-issues |
| **Identificación** | ID único del Work Item | ID de Issue |
| **Resultado / evidencia** | Qué produjo el trabajo y dónde encontrarlo | — |

Si LAPIN cambia de herramienta, se revisa esta tabla y se redefine solo la columna de implementación — el modelo (columnas 1 y 2) no cambia.

---

## 4. Work Item Type

Jerarquía: `EPIC → USER STORY → TASK`. `BUG` es un tipo aparte, no jerárquico.

| Tipo | Uso |
|---|---|
| **EPIC** | Objetivo o iniciativa amplia que agrupa trabajo relacionado. Funciona como contenedor, no necesariamente como trabajo ejecutable. |
| **USER STORY** | La unidad principal de trabajo de LAPIN. Persigue un resultado identificable y verificable. |
| **TASK** | Parte de una User Story que necesita seguimiento independiente. No toda User Story necesita Tasks — solo si el paso requiere estado o gestión propia. |
| **BUG** | Corrección de un comportamiento existente. Se mantiene separado para medir específicamente el trabajo de corrección. |

---

## 5. Rol responsable

Identifica qué Rol de LAPIN tiene la responsabilidad funcional sobre el trabajo — **independiente de quién opera la herramienta**. Una persona puede crear o mover un Work Item sin ser responsable de él.

La definición oficial de Roles vive en la documentación de Roles de LAPIN, no acá, para evitar duplicarla.

Debe poder usarse para: identificar responsabilidad, visualizar, filtrar, agrupar y generar métricas. Cuando sea posible, cada Rol debe distinguirse visualmente (color/ícono).

---

## 6. Activity Type

Independiente del Work Item Type y del Rol responsable — un mismo Rol puede hacer distintos tipos de actividad.

| Activity Type | Cuándo usarlo |
|---|---|
| **ANÁLISIS** | Investigación, evaluación de alternativas, requisitos, factibilidad |
| **DESARROLLO** | Programación, implementación, integraciones |
| **DOCUMENTACIÓN** | Crear o actualizar documentación formal |
| **GESTIÓN** | Planificación, seguimiento, coordinación |
| **CONFIGURACIÓN** | Configurar herramientas, campos, workflows, permisos |
| **DISEÑO** | UI/UX, diseño gráfico, identidad visual, prototipos |
| **TESTING / QA** | Pruebas, validación, detección de errores |
| **AUTOMATIZACIÓN** | Diseño e implementación de procesos automáticos |
| **INFRAESTRUCTURA** | Bases de datos, despliegues, hosting, entornos |
| **COMUNICACIÓN** | Contenido, publicaciones, difusión institucional |
| **CAPACITACIÓN** | Aprendizaje orientado a adquirir conocimiento necesario |
| **DIRECCIÓN Y ESTRATEGIA** | Objetivos, estrategia, prioridades, decisiones organizacionales |
| **RECURSOS HUMANOS** | Gestión y estructura de integrantes de LAPIN |

**Regla:** Work Item Type = qué unidad es · Activity Type = qué naturaleza tiene · Rol responsable = quién responde por él.

---

## 7. Status

`BACKLOG → TO DO → IN PROGRESS → IN REVIEW → DONE`

`BLOCKED` es un estado temporal dentro de `IN PROGRESS` (`IN PROGRESS → BLOCKED → IN PROGRESS`). Una actividad puede volver a un estado anterior si la realidad del trabajo lo requiere. El workflow suma estados solo ante una necesidad real.

---

## 8. Priority

`URGENT` (atención inmediata) · `HIGH` · `MEDIUM` (normal) · `LOW` (puede esperar sin impacto). La representación visual puede variar según la herramienta, pero debe distinguirse a simple vista.

---

## 9. Estimate

Story Points en escala Fibonacci: `1 · 2 · 3 · 5 · 8 · 13` (considerando complejidad, volumen e incertidumbre juntos — **no son horas**). `13` es señal de evaluar dividir el Work Item. Las horas reales viven en el sistema de time tracking (sección 17).

---

## 10. Iteration

Organiza Work Items por período de trabajo, para poder observar: trabajo planificado vs. terminado vs. pendiente, producción por período y evolución de la capacidad. La duración de las iteraciones puede ajustarse con la experiencia.

---

## 11. Fechas

| Campo | Significado |
|---|---|
| **Created** | Cuándo se creó el Work Item |
| **Start Date** | Cuándo empezó efectivamente |
| **Updated** | Última actualización |
| **Due Date** | Cuándo se espera que termine |
| **Finish Date** | Cuándo terminó efectivamente |

Mantener `Created ≠ Start Date` y `Due Date ≠ Finish Date` como campos distintos permite comparar planificación vs. ejecución real.

---

## 12. Labels

Clasificación complementaria que no duplica lo que ya cubren Work Item Type, Activity Type, Rol responsable, Status o Priority. Un Label complementa la estructura, no la reemplaza.

---

## 13. Relaciones y jerarquía

Jerarquía estándar: `EPIC → USER STORY → TASK`. Cada Work Item necesita un identificador único (no depender del título) para trazabilidad, integraciones, automatizaciones y registro de horas. La herramienta puede llamar a estas relaciones Parent/Child, Sub-issue u otro nombre equivalente sin que cambie el modelo.

---

## 14. Resultado y evidencia

Todo Work Item gestionable persigue un resultado identificable: una decisión, documentación, código, diseño, configuración, análisis, conocimiento obtenido por experimento, u otro resultado verificable. Cuando existe evidencia concreta, debe poder vincularse al Work Item.

---

## 15. Vistas y visualización

La estructura de los datos y su visualización son cosas distintas: los mismos Work Items pueden mostrarse en distintas vistas (operativa, por EPIC, por Rol, por Iteration, por tipo) según la necesidad. No se crean vistas preventivamente — una vista existe porque responde una necesidad de gestión.

La vista operativa debe permitir ver de un vistazo: cantidad de trabajo, estado, Rol responsable, prioridad y bloqueos, sin abrir cada Work Item individualmente.

---

## 16. Métricas y time tracking

Los parámetros estructurados (Work Item → Type → Activity Type → Rol → Estimate → Iteration → Fechas → Resultado) permiten analizar qué tipo de trabajo se produce, qué Roles participan, cómo se distribuye y cómo evoluciona la capacidad.

`Estimate` y `time tracking` son dimensiones distintas: Estimate mide tamaño/complejidad relativa; time tracking mide esfuerzo humano real invertido. El sistema de gestión debe poder relacionar cada Work Item con su registro de horas correspondiente (documentado aparte). Juntos permiten ver cuánto esfuerzo humano requiere cada tipo de resultado.

---

## 17. Escalabilidad y fricción operativa

La separación entre datos estructurados y vistas permite que el modelo crezca (nuevos proyectos, productos o líneas de trabajo) sin crear sistemas aislados — solo se agrega un dato estructurado nuevo cuando aparece una necesidad real de distinguir esas líneas, no antes.

Por el mismo motivo, se evita: crear campos o Labels sin necesidad, crear Tasks para microacciones, crear vistas sin una pregunta concreta que respondan, y duplicar información. Mantener el sistema no debe convertirse en el trabajo.

---

## 18. Preparación para automatización

La estructura debe ser suficientemente precisa para que una automatización o IA la opere sin decidir por su cuenta qué son los tipos, roles, estados o valores válidos — debe usar las reglas y nomenclaturas ya definidas acá (campos estructurados, IDs únicos, relaciones jerárquicas, valores normalizados), no reconstruir información interpretando texto libre cuando existe un campo estructurado disponible.

> La automatización implementa el modelo. No lo reinterpreta.

---

## 19. Evolución del modelo

Este modelo no es definitivo. Cambia cuando el uso real detecta información faltante, parámetros innecesarios, problemas de usabilidad o nuevas necesidades de medición — nunca de forma preventiva porque una herramienta lo permite.

**El modelo debe poder sobrevivir a la herramienta.**