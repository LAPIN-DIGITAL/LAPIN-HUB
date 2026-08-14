
>**Versión:** 1.0 | 
>**Fecha:** 14/08/2026 | 
>**Autor:** Jessica
> ---
> 
# Elección de Jira como herramienta de gestión de tareas

## Contexto

A medida que LAPIN DIGITAL comenzó a crecer, apareció una necesidad que la documentación existente en GitHub no resolvía por sí sola.

GitHub permite conservar muy bien la historia del proyecto: qué se hizo, qué decisiones se tomaron y por qué. Sin embargo, al retomar el trabajo después de algunos días, resultaba difícil responder rápidamente preguntas simples como:

* ¿Dónde había quedado?
* ¿Qué estaba haciendo?
* ¿Qué falta hacer?
* ¿Qué rol tiene tareas pendientes?
* ¿Qué debería hacerse a continuación?

Era necesario incorporar una herramienta para gestionar el **trabajo presente y futuro**, complementando la documentación histórica que ya existe en GitHub.

## Qué se buscó

La herramienta debía cumplir algunos criterios básicos:

* Tener un tablero visual y fácil de leer.
* Permitir trabajar con tareas o tarjetas.
* Identificar qué rol es responsable de cada tarea.
* Mostrar claramente qué está pendiente, en curso, bloqueado o terminado.
* Permitir retomar fácilmente el trabajo después de varios días.
* Ser simple de mantener.
* Tener una opción gratuita que permita utilizarla de manera permanente.
* Preferentemente, aportar aprendizaje sobre una herramienta utilizada profesionalmente en gestión de proyectos.

La intención no era incorporar una herramienta solamente porque tuviera muchas funcionalidades, sino encontrar una solución **buena, visual, práctica y económica**.

## Herramientas consideradas

Se consideraron principalmente:

* **Azure DevOps Boards:** herramienta ya conocida y utilizada profesionalmente, pero justamente por eso aportaba poco aprendizaje nuevo.
* **GitHub Projects:** tenía la ventaja de estar integrado directamente con los repositorios y la documentación de LAPIN.
* **Trello:** muy simple y visual, especialmente atractivo para trabajar con un modelo similar a tarjetas físicas.
* **Jira:** herramienta ampliamente utilizada para gestión de proyectos y equipos de tecnología, con una estructura visual de tableros y tareas.

## Decisión

Se decidió comenzar utilizando **Jira Free**.

La elección se basó principalmente en que combina:

**gestión visual + simplicidad suficiente + aprendizaje profesional + costo inicial cero.**

Jira permite representar el trabajo mediante tarjetas y visualizar rápidamente el estado general del proyecto, algo especialmente importante para LAPIN, ya que el proyecto no se trabaja necesariamente todos los días.

Además, existe una versión gratuita permanente adecuada para la escala actual de LAPIN DIGITAL, por lo que es posible utilizar la herramienta en un proyecto real sin depender de un período de prueba limitado.

Otro factor importante fue el aprendizaje.

Azure DevOps ya forma parte de las herramientas utilizadas habitualmente, por lo que incorporar Jira permite experimentar con otra herramienta ampliamente utilizada en proyectos tecnológicos mientras se gestiona un proyecto real.

## Separación de responsabilidades entre herramientas

Por el momento se establece la siguiente separación:

### GitHub

Será principalmente la **memoria del proyecto**.

Contendrá:

* decisiones;
* evolución;
* documentación;
* conocimiento generado;
* código y repositorios;
* ejemplos o archivos que tenga sentido conservar junto al proyecto.

### Jira

Será principalmente la **gestión del trabajo**.

Permitirá visualizar:

* qué hay que hacer;
* qué se está haciendo;
* qué está bloqueado;
* qué está terminado;
* qué rol debe realizar cada tarea;
* qué debería hacerse a continuación.

De esta manera:

> **GitHub registra el camino recorrido. Jira muestra dónde estamos y qué falta hacer.**

## Consideración futura

La elección de Jira no se considera irreversible.

LAPIN DIGITAL es también un espacio de experimentación, por lo que la herramienta será evaluada mediante su uso real.

Si con el crecimiento del proyecto Jira deja de resultar conveniente por costos, limitaciones o integración con otras herramientas, podrá reemplazarse manteniendo el modelo de trabajo y migrando las tareas necesarias.

La herramienta acompaña el proceso; **no define el proceso**.
