# Configurar Jira

Una vez que elegimos **Jira Free** para gestionar LAPIN HUB apareció la siguiente pregunta:

**¿Cómo configuramos una herramienta pensada para gestionar equipos de personas cuando nuestro equipo está formado por especialistas que pueden ser humanos o IA?**

No queríamos configurar Jira simplemente siguiendo todas las opciones que ofrece.

Queríamos que Jira representara **cómo funciona LAPIN**.

---

## El problema principal: representar a nuestros especialistas

En Jira normalmente una actividad puede asignarse a un usuario.

En LAPIN eso no alcanza.

Actualmente una persona puede operar Jira y realizar los clics necesarios, mientras que el trabajo pertenece intelectualmente a otro especialista.

Por ejemplo:

> **Historia:** Configurar Jira
> **Rol responsable:** Jira Administrator

La persona que mueve esa Historia dentro de Jira no necesariamente es quien produjo el conocimiento o tomó las decisiones representadas por ella.

Además, nuestros roles son dinámicos.

Un especialista puede ser IA o humano, incorporarse cuando aparece una necesidad, evolucionar o incluso dejar de ser necesario.

Crear un usuario de Jira para representar cada rol no reflejaría correctamente este modelo.

---

## Rol responsable

Esta necesidad llevó a una de las decisiones principales de la configuración:

> **Crear un campo propio llamado `Rol responsable`.**

El campo identifica **qué especialista de LAPIN es responsable del trabajo representado por una actividad**.

A partir de esta decisión, `Rol responsable` se convirtió en uno de los datos centrales de nuestra gestión.

Toda unidad de trabajo que ejecutemos deberá permitir identificar su rol responsable.

Esto nos permitirá observar el trabajo de LAPIN desde una perspectiva que nos interesa especialmente en este experimento:

**qué están haciendo nuestros distintos especialistas y cómo participa cada uno en la construcción de LAPIN.**

---

## Por qué no utilizamos etiquetas para los roles

También podríamos haber representado los roles mediante etiquetas.

Decidimos no hacerlo.

Las etiquetas son útiles para clasificar libremente una actividad:

`jira` · `github` · `documentacion` · `chatgpt` · `integracion`

Pero los roles representan una dimensión estructural de nuestra organización.

Necesitamos que sean consistentes porque queremos poder **filtrarlos, consultarlos y medirlos**.

La diferencia quedó así:

**Rol responsable** → ¿Qué especialista es responsable de este trabajo?

**Responsable de Jira** → ¿Qué usuario está gestionando la actividad dentro de Jira?

**Etiqueta** → ¿De qué trata o con qué se relaciona esta actividad?

Esta separación nos permite utilizar Jira sin confundir al especialista que produce el trabajo con la persona que opera la herramienta.

---

## Queremos poder observar cómo trabaja LAPIN

El campo `Rol responsable` también condicionó qué información necesitamos registrar alrededor de cada actividad.

Queremos poder combinar:

**Rol responsable + Sprint + Story Points + Estado**

para empezar a responder preguntas como:

* ¿Qué trabajo realizó cada rol?
* ¿Qué especialistas participaron durante un Sprint?
* ¿Cómo se distribuye el trabajo?
* ¿Cuántos Story Points completó cada rol?
* ¿Qué trabajo permanece pendiente?
* ¿Dónde aparecen bloqueos?
* ¿Cómo evoluciona la participación de los especialistas?

Estas métricas no buscan evaluar si un especialista es “mejor” que otro.

Buscan generar datos que nos permitan **observar y entender cómo funciona nuestro modelo de trabajo**.

---

## Sprints mensuales

Para comenzar decidimos utilizar **Sprints mensuales**.

Necesitamos períodos que nos permitan detenernos y observar qué ocurrió:

qué planificamos, qué terminamos, qué quedó pendiente, cuánto trabajo realizamos y qué roles participaron.

Elegimos un mes porque hoy nos parece un período razonable para obtener esa fotografía sin agregar demasiada gestión.

No consideramos esta duración definitiva.

Si la experiencia demuestra que otro período funciona mejor, lo cambiaremos.

---

## Un workflow pequeño

También mantuvimos el flujo de trabajo simple:

**TO DO → IN PROGRESS ↔ BLOCKED → IN REVIEW → DONE**

Agregamos `BLOCKED` porque necesitamos distinguir una actividad que simplemente está en ejecución de otra que **no puede continuar por algún impedimento**.

Eso además permitirá observar posteriormente qué bloqueos aparecen y a qué roles afectan.

No agregamos estados adicionales, como QA, porque hoy no tenemos una necesidad que los justifique.

Si aparece, lo incorporaremos.

---

## Qué trabajo queremos registrar

Otro problema fue decidir cuánto detalle llevar a Jira.

Configurar Jira, por ejemplo, implicó crear campos, configurar estados, modificar opciones y realizar distintas pruebas.

Podríamos haber creado una actividad para cada una.

Decidimos no hacerlo.

Nos interesa registrar **unidades de trabajo que produzcan un resultado identificable**, no cada acción necesaria para conseguirlo.

Por eso:

> **Historia: Configurar Jira**

puede ser suficiente para representar todo ese trabajo.

Inicialmente utilizaremos principalmente:

**Historia + Error**

Epic y Función servirán para agrupar trabajo de mayor alcance.

Tarea y Subtarea quedarán disponibles para cuando realmente necesitemos dividir una actividad.

Esto evita que mantener Jira termine generando más trabajo que el propio trabajo que queremos gestionar.

---

## Story Points

Utilizaremos **Story Points** para comenzar a estimar el esfuerzo relativo de las unidades de trabajo que ejecutamos.

Nos interesa especialmente poder relacionarlos con los Sprints y los Roles responsables para observar cómo evoluciona el sistema.

No estimaremos todos los niveles de la estructura simultáneamente si eso provoca duplicaciones.

Tampoco consideraremos los Story Points una medida absoluta de productividad.

Son una herramienta para **observar capacidad, esfuerzo y evolución**.

---

## Qué decidimos no configurar

Jira permite configurar muchísimo más.

Deliberadamente decidimos no hacerlo.

Por ahora no necesitamos:

* usuarios artificiales para representar especialistas;
* más estados en el workflow;
* campos sin una necesidad concreta;
* un catálogo cerrado de etiquetas;
* utilizar Tareas y Subtareas para cada pequeña acción;
* estimar todos los niveles del trabajo;
* automatizaciones que todavía no resuelven un problema real;
* estructuras adicionales simplemente porque Jira las permite.

Esto no significa que nunca vayamos a utilizarlas.

Significa que **todavía no tenemos evidencia de que las necesitemos**.

---

## Qué quedó configurado

La estructura inicial quedó preparada para comenzar a trabajar con:

**Proyecto:** LAPIN HUB
**Clave:** `LHB`
**Sprints:** mensuales
**Workflow:** TO DO → IN PROGRESS ↔ BLOCKED → IN REVIEW → DONE
**Campo central:** Rol responsable
**Estimación:** Story Points
**Clasificación flexible:** Etiquetas
**Unidad principal de trabajo:** Historia + Error

La estructura podrá crecer cuando el trabajo real lo requiera.

---

## Qué queremos aprender

Esta configuración no es solamente una forma de ordenar tareas.

Forma parte del experimento de LAPIN HUB.

Queremos comprobar si podemos gestionar el trabajo de distintos especialistas humanos e IA, conservar quién fue responsable de cada resultado y generar información que nos permita entender cómo funciona este modelo organizacional.

Por eso `Rol responsable` terminó siendo el centro de la configuración.

No configuramos Jira alrededor de quién hace clic en una actividad.

Lo configuramos alrededor de **quién aporta el trabajo que esa actividad representa**.

Y a partir de ahora podremos empezar a observarlo.

> **Jira debe ayudarnos a representar y entender cómo trabaja LAPIN. La configuración evolucionará cuando la experiencia nos demuestre que necesitamos algo más.**
