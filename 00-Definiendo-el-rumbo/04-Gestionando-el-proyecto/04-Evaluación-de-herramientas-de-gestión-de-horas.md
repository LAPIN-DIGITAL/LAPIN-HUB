> **Versión:** 1.0
> **Fecha:** 19/08/2026
> **Autor:** Jessica & Work Management Administrator IA
> **Revisado:** Quality Assurance & Review IA

# Importancia de incorporar un sistema de gestión de horas

## Por qué apareció la necesidad

LAPIN ya resolvió cómo documentar el conocimiento (LAPIN HUB) y cómo gestionar el trabajo (sistema de gestión, Work Items). Pero falta una dimensión que ninguno de los dos cubre: **cuánto tiempo humano real cuesta operar este modelo**.

Ninguna IA trabaja sola. Cada Work Item que avanza — una tarjeta documentada, una decisión tomada, una herramienta configurada — requiere que una persona interactúe, oriente, revise y decida. Ese tiempo humano es el verdadero costo del proyecto, y hoy no se está midiendo.

Sin ese dato, preguntas simples quedan sin respuesta:

- ¿Cuánto tiempo humano llevó el onboarding de todos los Roles de LAPIN?
- ¿Cuánto tiempo humano llevó producir la documentación, el conocimiento, el producto de valor generado hasta ahora?
- ¿Este experimento es productivo comparado con un proyecto equivalente hecho de forma tradicional?

Sin registro de horas, LAPIN puede decir *qué* se hizo, pero no *a qué costo humano*.

> LAPIN HUB conserva el conocimiento. El sistema de gestión conserva el estado del trabajo. El sistema de horas conserva el costo humano de haberlo hecho.

---

## El tiempo como variable central del experimento

El tiempo de la IA es relativo y no comparable — no define el costo real de nada. El tiempo humano sí. Es el recurso escaso, el que permite comparar este modelo contra cualquier otra forma de trabajar.

En cualquier proyecto — con equipo humano tradicional o con este modelo de Roles IA — el tiempo es una de las variables centrales del éxito. Un resultado no vale lo mismo si costó un mes de esfuerzo humano que si costó cinco. Sin ese dato, no hay forma real de evaluar si orquestar un equipo virtual de especialistas IA es, en la práctica, más productivo que la alternativa.

---

## Qué se mide

Se mide el **tiempo humano real insumido**, independientemente de:

- **quién** lo hizo (cualquier persona que opere un Rol, no solo quien orquesta el proyecto);
- **qué Rol** estaba operando en ese momento (CEO, Developer, RRHH, Knowledge & Documentation, etc.);
- **cuánto avanzó** el Work Item gracias a la IA.

Lo que se registra es el costo humano de trabajar esa unidad de trabajo — no el desempeño de la IA.

Cada persona puede estar trabajando en paralelo sobre distintas tarjetas con distintos Roles. Cada una de esas interacciones es tiempo humano insumido en el proyecto, y debe poder sumarse al total.

---

## Para qué se usan los datos

### 1. Medición retrospectiva del experimento

Permite responder, con datos reales y no estimaciones, cuánto costó en tiempo humano cada resultado: el onboarding de los Roles, la documentación generada, cada producto de valor entregado. Es la base para comparar la productividad de este modelo contra la de un proyecto equivalente hecho de forma tradicional.

### 2. Señal para decisiones sobre la marcha

No todo el tiempo invertido genera resultado útil. Cuando una línea de trabajo consume tiempo humano sin llegar a un resultado válido — como ocurrió con la evaluación de Jira, descartada tras no ajustarse al modelo de gestión de LAPIN — ese tiempo también es información valiosa.

Sin registrarlo, una decisión descartada deja de ser aprendizaje medible y se convierte en una sensación no verificable. Registrar el tiempo, incluso el que no llegó a buen puerto, permite distinguir:

- tiempo que generó resultado directo;
- tiempo que generó aprendizaje (una alternativa descartada con motivo documentado);
- tiempo que se perdió sin dejar ningún resultado aprovechable.

> El éxito del experimento no se mide solo por lo que funcionó. También se mide por cuánto costó descubrir qué no funcionaba.

---

## Relación con el sistema de gestión existente

Esta necesidad no es independiente del sistema de gestión ya definido. La Estructura y configuración del sistema de gestión ya anticipó esta relación: *Estimate* mide tamaño o complejidad relativa de un Work Item; *time tracking* mide el esfuerzo humano real invertido en trabajarlo. Son dimensiones distintas y complementarias.

Por eso, todo registro de horas debe poder vincularse a un Work Item existente (EPIC, USER STORY, TASK o BUG) y, a través de él, a un Rol responsable y un Activity Type. Esto permite eventualmente cruzar: tipo de trabajo + Rol + tiempo estimado + tiempo humano real, y entender qué tipo de trabajo consume más esfuerzo humano de lo esperado.

La herramienta que finalmente implemente este registro es una decisión posterior. Como ocurrió con el sistema de gestión, primero se define la necesidad y el modelo — recién después se evalúan herramientas que puedan representarlo.

---

## Qué queda pendiente definir

Este documento establece la necesidad y el criterio de uso de los datos. Quedan fuera de su alcance — y corresponden a un documento posterior de modelo/estructura, análogo al que ya existe para el sistema de gestión —:

- cómo se registra cada bloque de tiempo (granularidad, unidad de medida);
- si el registro es manual, asistido o automatizado;
- qué herramienta lo implementa y cómo se relaciona técnicamente con el Work Item correspondiente;
- qué reportes o vistas se necesitan para consumir esta información.

Esa evaluación ya se realizó y está documentada en *Evaluación de herramientas de gestión de horas que se amoldan al modelo*.