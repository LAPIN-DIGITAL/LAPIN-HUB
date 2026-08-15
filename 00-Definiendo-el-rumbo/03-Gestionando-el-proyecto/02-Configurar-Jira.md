# Configuración inicial de Jira para LAPIN HUB

## Contexto

Luego de evaluar distintas herramientas de gestión y seleccionar **Jira Free** para gestionar el trabajo de LAPIN HUB, se realizó una primera configuración de la herramienta.

El objetivo de esta etapa no fue configurar todas las capacidades disponibles en Jira, sino preparar una estructura mínima que permita comenzar a trabajar, registrar actividades y obtener información útil sobre el trabajo realizado.

Se tomó como criterio general:

> **Configurar solamente aquello que responde a una necesidad actual.**

La configuración podrá evolucionar a medida que el uso real permita identificar nuevas necesidades.

---

# 1. Proyecto

Se creó un espacio de trabajo para:

**LAPIN HUB**

Se definió la siguiente clave:

`LHB`

Esta clave permitirá identificar las actividades del proyecto mediante códigos como:

`LHB-1`
`LHB-2`
`LHB-3`

---

# 2. Gestión mediante Sprints

Se decidió comenzar utilizando **Sprints mensuales**.

El primer Sprint finalizará junto con el mes en curso.

La intención inicial es utilizar períodos mensuales para poder observar progresivamente:

* cantidad de trabajo realizado;
* trabajo planificado frente a trabajo terminado;
* distribución del trabajo entre roles;
* Story Points completados;
* actividades que permanecen pendientes;
* evolución de la capacidad de trabajo de LAPIN.

Esta estructura podrá revisarse posteriormente si la experiencia demuestra que otra duración resulta más conveniente.

---

# 3. Backlog

El Backlog será utilizado como espacio para mantener actividades identificadas que todavía no fueron priorizadas para ejecución.

Durante la planificación de cada Sprint se podrá revisar este conjunto de trabajo y seleccionar qué actividades pasarán a formar parte del trabajo próximo.

El Backlog no representa un estado del workflow.

Representa una instancia de **planificación y priorización**.

Una actividad no finalizada durante un Sprint podrá regresar al Backlog si se decide no priorizarla para el período siguiente.

---

# 4. Workflow inicial

Se definió el siguiente flujo de trabajo:

**TO DO → IN PROGRESS → IN REVIEW → DONE**

Además se incorporó:

**BLOCKED**

El estado `BLOCKED` representa actividades que no pueden continuar temporalmente debido a una dependencia, información pendiente, decisión, insumo u otro impedimento.

Una actividad bloqueada puede volver a ejecución cuando desaparezca el impedimento:

**IN PROGRESS → BLOCKED → IN PROGRESS**

`BLOCKED` pertenece a la categoría **In Progress**, ya que el trabajo continúa abierto y no debe considerarse terminado.

No se incorporaron estados adicionales como QA debido a que actualmente no existe una necesidad que los justifique.

La estructura inicial queda:

**TO DO → IN PROGRESS ↔ BLOCKED → IN REVIEW → DONE**

---

# 5. Rol responsable

Se creó el campo personalizado:

**Rol responsable**

Su objetivo es identificar qué especialista de LAPIN es responsable de producir el trabajo representado por una actividad.

Ejemplos:

* CEO
* Knowledge & Documentation
* UI/UX Designer
* Sr. Developer
* Jira Administrator

Este campo no representa necesariamente quién realiza físicamente las acciones dentro de Jira.

Actualmente la operación de la herramienta puede realizarse manualmente por una persona, mientras que la responsabilidad intelectual o funcional continúa perteneciendo al rol correspondiente.

Por ejemplo:

> **Actividad:** Configurar Jira
> **Rol responsable:** Jira Administrator

Aunque otra persona realice manualmente los clics necesarios dentro de Jira, el trabajo continúa siendo responsabilidad del Jira Administrator.

Esta distinción será especialmente importante al analizar posteriormente la participación y producción de los distintos roles de LAPIN.

---

# 6. Importancia de Rol responsable para las métricas

El campo `Rol responsable` permitirá posteriormente analizar información como:

* cantidad de actividades realizadas por rol;
* Story Points completados por rol;
* distribución del trabajo;
* actividades bloqueadas;
* trabajo pendiente;
* evolución de la participación de cada especialista.

Esto permitirá comenzar a generar datos sobre el funcionamiento real de una organización basada en especialistas IA.

Se establece como criterio inicial:

> **Toda unidad de trabajo ejecutable deberá identificar su Rol responsable.**

---

# 7. Etiquetas

Se decidió utilizar el campo estándar de Jira:

**Etiquetas**

Las etiquetas permitirán clasificar transversalmente las actividades cuando resulte útil.

No se definirá anticipadamente un catálogo completo de etiquetas.

Las etiquetas se crearán **por demanda y necesidad**, evitando generar clasificaciones que posteriormente no tengan utilidad.

Ejemplos futuros podrían ser:

`jira`
`github`
`documentacion`
`chatgpt`
`integracion`

Las etiquetas representan de qué trata o con qué se relaciona una actividad.

No deben utilizarse para representar el rol responsable, ya que esa información posee un campo estructurado propio.

---

# 8. Tipos de actividad

Se decidió mantener disponibles los siguientes tipos de actividad:

## Epic

Representa una iniciativa u objetivo amplio.

Puede contener trabajo correspondiente a distintos especialistas.

Por este motivo no necesariamente tendrá un único Rol responsable.

---

## Función

Representa una capacidad o conjunto amplio de trabajo relacionado dentro de una Epic.

Puede utilizarse para agrupar varias Historias relacionadas.

Ejemplo:

> **Epic:** Implementar la gestión operativa de LAPIN HUB
> **Función:** Implementar Jira como herramienta de gestión

---

## Historia

Será inicialmente la **unidad principal de trabajo de LAPIN**.

Representará un resultado suficientemente significativo como para que resulte útil registrar que fue realizado.

Ejemplos:

* Evaluar herramientas de gestión.
* Configurar Jira.
* Estructurar el backlog.
* Integrar Jira con ChatGPT.
* Evaluar el resultado de una automatización.

---

## Error

Representará un comportamiento existente que no funciona de la manera esperada y necesita ser corregido.

Mantenerlo separado de Historia permitirá posteriormente observar y medir específicamente el trabajo dedicado a correcciones.

---

## Tarea

Se mantiene disponible para situaciones donde resulte útil representar trabajo técnico u operativo específico.

Inicialmente LAPIN no necesita utilizarla de manera habitual.

---

## Subtarea

Se mantiene disponible para aquellos casos donde resulte necesario dividir una actividad en unidades menores.

Inicialmente tampoco será utilizada de manera habitual.

---

# 9. Granularidad del trabajo

Se decidió evitar una fragmentación excesiva de las actividades.

Jira debe registrar **unidades de trabajo con un resultado identificable**, no cada acción realizada para conseguirlo.

Por ejemplo, configurar Jira puede requerir:

* crear campos;
* agregar valores;
* configurar estados;
* modificar transiciones;
* configurar tipos de actividad.

Esto no implica necesariamente crear una actividad independiente para cada acción.

Podrá registrarse simplemente como:

> **Historia: Configurar Jira**

Los detalles internos podrán incluirse en la descripción cuando tengan valor.

Este criterio busca evitar que mantener Jira genere una carga administrativa superior al beneficio obtenido.

También evita distorsionar las métricas mediante grandes cantidades de actividades pequeñas que no representan resultados independientes.

---

# 10. Story Points

Se utilizarán Story Points para comenzar a estimar y observar el trabajo realizado.

Como criterio inicial, la estimación se concentrará principalmente en las unidades de trabajo que realmente se ejecutan y miden.

Inicialmente:

* **Historia:** puede estimarse.
* **Error:** puede estimarse.
* **Tarea:** podrá estimarse si comienza a utilizarse como unidad independiente.
* **Epic:** no se estimará.
* **Función:** no se estimará.
* **Subtarea:** inicialmente no se estimará.

Se evitará estimar simultáneamente una actividad y todos sus componentes cuando eso pueda provocar duplicación en las métricas.

---

# 11. Estructura resultante

La estructura conceptual inicial de Jira para LAPIN HUB queda definida como:

**EPIC**
↓
**FUNCIÓN**
↓
**HISTORIA / ERROR**
↓
**TAREA / SUBTAREA**, únicamente cuando exista una necesidad que justifique utilizarlas.

En la operación inicial se priorizará principalmente el uso de:

**Historia + Error**

El resto de los tipos permanecerá disponible para cuando la complejidad real del trabajo requiera utilizarlos.

---

# 12. Principio de simplicidad

La configuración inicial de Jira no se considera definitiva.

La herramienta evolucionará a partir de necesidades detectadas durante su utilización.

No se agregarán:

* campos;
* workflows;
* estados;
* tipos;
* automatizaciones;
* métricas;
* estructuras;

solamente porque Jira permita hacerlo.

Cada incorporación deberá resolver un problema concreto.

> **Jira debe facilitar la gestión de LAPIN, no convertirse en una nueva tarea que LAPIN tenga que gestionar.**

---

# Próximo paso

Con la configuración inicial disponible, el siguiente paso será comenzar a estructurar el trabajo real de LAPIN HUB mediante:

**Epic → Función → Historias**

A partir del uso real se evaluará si la configuración actual resulta suficiente o necesita evolucionar.

Posteriormente se analizará la integración y automatización entre **Jira y ChatGPT**, con el objetivo de reducir progresivamente la intervención manual necesaria para mantener actualizado el sistema de gestión.
