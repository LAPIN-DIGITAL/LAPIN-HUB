> **Versión:** 1.0
> **Fecha:** 19/08/2026
> **Autor:** Work Management Administrator + LAPIN Knowledge & Documentation

# Evaluación de herramientas de gestión de horas que se amoldan al modelo

> Este documento complementa a *Importancia de incorporar un sistema de gestión de horas*, donde se define **por qué** LAPIN necesita medir esfuerzo humano y para qué se usan esos datos. Acá se documenta **cómo se evaluaron** las alternativas disponibles y **qué se decidió** en consecuencia.

## Contexto

Una vez definido e implementado el sistema de gestión de trabajo de LAPIN, surgió la necesidad de incorporar una segunda dimensión de medición:

**cuánto esfuerzo humano requiere realizar el trabajo gestionado por LAPIN.**

GitHub Projects permite conocer qué actividades existen, su estado, prioridad, estimación, Rol responsable, tipo de actividad y demás información necesaria para gestionar el trabajo.

Sin embargo, LAPIN también necesita poder responder:

- ¿Cuántas horas humanas requirió una actividad?
- ¿Cuánto tiempo se invirtió en un Issue determinado?
- ¿Cuántas horas se utilizaron por día, semana, mes o año?
- ¿Qué Roles demandan mayor intervención humana?
- ¿En qué tipos de actividad se consume el tiempo?
- ¿Cómo evoluciona ese esfuerzo a medida que LAPIN incorpora automatización?

Por este motivo se inició la evaluación de herramientas de gestión de horas.

---

## Qué queremos medir

El objetivo no es medir cuánto tiempo "trabaja" una IA.

Los Roles de LAPIN son especializaciones asignadas a diferentes integrantes IA y no representan personas físicas que deban registrar una jornada laboral.

Lo que interesa medir es:

> **el esfuerzo humano necesario para producir, gestionar, revisar y materializar el trabajo realizado dentro de LAPIN.**

Por lo tanto, se estableció la siguiente separación:

**GitHub Projects** registra qué trabajo realiza LAPIN.

**El sistema de gestión de horas** registra cuánto esfuerzo humano requiere ese trabajo.

Ambos sistemas deben poder relacionarse mediante la actividad gestionada en GitHub.

---

## Necesidades identificadas

Durante la investigación se determinó que el sistema de horas debe permitir como mínimo:

- asociar tiempo a una actividad existente en GitHub;
- identificar la actividad mediante Issue y título;
- registrar múltiples períodos de trabajo sobre una misma actividad;
- conservar el detalle histórico de cada registro;
- obtener el total acumulado por Issue;
- consultar horas por día;
- consultar horas por semana;
- consultar horas por mes;
- consultar horas por año;
- analizar horas por Rol;
- analizar horas por tipo de actividad;
- corregir registros;
- mantener una operación de muy baja fricción.

La herramienta de horas no debe convertirse en un segundo sistema de gestión ni obligar a mantener manualmente información que ya existe en GitHub.

---

## Primer enfoque: utilización de timers

Inicialmente se evaluaron herramientas tradicionales de time tracking basadas principalmente en el mecanismo:

`START → trabajo → STOP`

Entre las alternativas consideradas estuvieron **Toggl Track** y **Clockify**.

Ambas ofrecen las funciones habituales de una herramienta de seguimiento de tiempo:

- temporizador;
- carga manual;
- historial;
- proyectos;
- reportes;
- integraciones;
- posibilidades de automatización mediante API.

A primera vista estas características parecían suficientes para cubrir la necesidad.

Sin embargo, al trasladar el funcionamiento al uso cotidiano de LAPIN apareció un problema operativo importante.

---

## Problema del timer

El registro mediante cronómetro depende de que la persona recuerde constantemente:

1. iniciar el timer;
2. detenerlo cuando deja una actividad;
3. cambiarlo cuando comienza otra;
4. volver a iniciarlo al retomar una actividad.

Esto introduce una nueva tarea administrativa dentro del trabajo.

Además, durante una jornada puede alternarse rápidamente entre diferentes actividades.

Por ejemplo:

`#12 → #15 → #12`

Si los timers no se administran correctamente, los registros pueden quedar incompletos o incluso contabilizar tiempo simultáneo que no representa esfuerzo humano real.

El sistema comenzaría entonces a producir datos aparentemente precisos pero conceptualmente incorrectos.

Se concluyó que:

> **La precisión de un sistema de horas no depende solamente de su capacidad de medir minutos, sino de que su mecanismo de registro pueda mantenerse correctamente durante el trabajo real.**

---

## Evaluación de Clockify

Clockify fue probado como posible solución.

Se verificó que permite crear proyectos, registrar tiempo, utilizar timers, realizar cargas manuales y posteriormente consultar reportes.

También ofrece posibilidades de integración y automatización.

Sin embargo, para el modelo de LAPIN continuaba existiendo una fricción importante: el registro debía mantenerse conscientemente mientras se alternaba entre actividades.

Además, no resultaba conveniente reconstruir dentro de Clockify las tareas, Roles y demás estructura que ya se encuentra administrada mediante GitHub Projects.

Se decidió no continuar invirtiendo tiempo en su configuración.

---

## Evaluación de Toggl Track

Toggl Track fue considerado por motivos similares:

- facilidad de registro;
- temporizador;
- carga manual;
- reportes;
- posibilidades de integración.

Sin embargo, compartía el mismo problema conceptual del enfoque basado principalmente en timers.

La herramienta podía registrar correctamente el tiempo siempre que la operación del cronómetro fuera mantenida correctamente por la persona.

Esto no resolvía el requisito principal de LAPIN:

**obtener información útil sin aumentar significativamente la carga administrativa.**

---

## Evaluación de Everhour

Posteriormente se analizó Everhour porque su integración con GitHub se aproximaba más al comportamiento buscado.

La posibilidad de asociar horas directamente con actividades de GitHub y realizar cargas manuales resultaba más cercana al modelo deseado.

Esta evaluación permitió identificar un aprendizaje importante:

> LAPIN no necesita necesariamente medir el trabajo mediante un cronómetro. Necesita poder imputar correctamente esfuerzo humano a una actividad.

Esto llevó a reconsiderar el requisito inicial.

En lugar de:

`iniciar timer → trabajar → detener timer`

el modelo deseado pasó a ser:

`actividad → registrar horas realizadas`

Por ejemplo:

`#12 → 2 horas`

Si posteriormente se vuelve a trabajar sobre la misma actividad:

`#12 → +1,5 horas`

El sistema debe conservar ambos registros y mostrar:

`Total #12 → 3,5 horas`

---

## Aprendizaje de la evaluación

La investigación permitió separar dos conceptos que inicialmente parecían equivalentes:

### Medición automática del tiempo

Busca registrar cuánto tiempo permanece activa una tarea o un cronómetro.

### Imputación de esfuerzo humano

Busca registrar cuánto esfuerzo humano fue realmente dedicado a una actividad.

Para LAPIN, la segunda dimensión resulta más importante.

La posibilidad de registrar manualmente horas después de una sesión de trabajo reduce la dependencia de mantener un timer permanentemente actualizado y se adapta mejor a una forma de trabajo donde pueden alternarse distintas actividades.

---

## Decisión sobre herramientas existentes

Las herramientas evaluadas son válidas como soluciones generales de time tracking.

El problema no es que carezcan de funcionalidades.

El problema es que fueron diseñadas para modelos de trabajo más amplios y diferentes al que LAPIN necesita actualmente.

Adoptarlas implicaría aceptar alguna combinación de:

- mayor fricción operativa;
- dependencia del uso correcto de timers;
- duplicación parcial de información;
- configuración adicional;
- adaptación del modelo de LAPIN a la herramienta;
- funcionalidades que no son necesarias para el laboratorio.

Por este motivo se decidió **no adoptar de forma definitiva ninguna de las herramientas evaluadas**.

---

# Decisión: desarrollar una solución propia

La necesidad real identificada es suficientemente pequeña y específica como para evaluar una solución propia.

Se decidió avanzar con el diseño de una aplicación de registro de horas desarrollada específicamente para LAPIN.

El principio será:

> **GitHub Projects administra el trabajo.  
> La aplicación de horas registra el esfuerzo humano.**

La nueva aplicación no deberá replicar:

- Issues;
- Status;
- prioridades;
- Iterations;
- jerarquías;
- gestión de tareas.

Esa información continuará perteneciendo a GitHub.

---

## Modelo esperado

Una entrada de tiempo deberá poder relacionarse con una actividad existente.

Como mínimo contendrá:

| Campo | Propósito |
|---|---|
| Fecha | Cuándo se realizó el trabajo |
| Issue | Identificador de la actividad |
| Título | Identificación humana de la actividad |
| Horas | Esfuerzo humano registrado |
| Rol | Rol LAPIN asociado |
| Actividad | Naturaleza del trabajo realizado |
| Notas | Información adicional opcional |

Una Issue podrá contener múltiples registros.

Ejemplo:

| Fecha | Issue | Horas | Actividad |
|---|---|---:|---|
| 16/08 | #12 | 2,0 | Análisis |
| 17/08 | #12 | 1,5 | Documentación |
| 19/08 | #12 | 3,0 | Análisis |

Resultado:

**Total Issue #12: 6,5 horas**

---

## Dimensiones de análisis

El sistema deberá permitir posteriormente analizar el esfuerzo humano desde diferentes perspectivas.

### Por Issue

Permite conocer cuánto esfuerzo requirió producir un resultado determinado.

### Por Rol

Permite conocer cuánto esfuerzo humano requiere el trabajo asociado a cada Rol LAPIN.

### Por Actividad

Permite conocer en qué naturaleza de trabajo se consumen las horas:

- análisis;
- desarrollo;
- documentación;
- gestión;
- configuración;
- diseño;
- testing / QA;
- automatización;
- infraestructura;
- comunicación;
- capacitación;
- dirección;
- recursos humanos.

### Por período

Debe poder analizarse el esfuerzo por:

- día;
- semana;
- mes;
- año.

---

# Solución transitoria

El desarrollo de la aplicación propia requiere análisis funcional, diseño técnico, implementación y validación.

Sin embargo, esperar a que el sistema estuviera desarrollado produciría una pérdida de información histórica.

Por este motivo se decidió comenzar inmediatamente el registro mediante una **planilla Excel transitoria**.

La planilla utiliza la misma estructura básica prevista para el futuro sistema:

`Fecha | Issue | Título | Horas | Rol | Actividad | Notas`

De esta manera, el período transitorio también genera información útil.

---

## Estructura de la planilla transitoria

La planilla dispone de pestañas mensuales para registrar las horas.

Utiliza catálogos controlados para:

- Rol;
- Actividad.

Además genera resúmenes:

- mensuales;
- anuales;
- por Rol;
- por Actividad;
- por Issue.

Esto permite comenzar a obtener métricas antes de que exista la aplicación definitiva.

---

## La planilla como prototipo funcional

La planilla no constituye únicamente una solución temporal.

También funciona como **prototipo funcional del futuro sistema**.

Su utilización permitirá descubrir:

- qué datos realmente se utilizan;
- qué información resulta innecesaria;
- qué reportes aportan valor;
- qué operaciones generan fricción;
- qué consultas se realizan con mayor frecuencia.

Por lo tanto, el futuro sistema no será diseñado únicamente a partir de requerimientos teóricos.

También podrá utilizar experiencia real obtenida durante el período de registro mediante Excel.

---

## Estrategia de migración

La información registrada durante esta etapa no deberá perderse.

El futuro sistema deberá contemplar la importación del histórico generado mediante la planilla.

El modelo previsto es:

`Excel → archivo de intercambio → aplicación → base de datos`

Los registros deberán conservar como mínimo:

- fecha;
- Issue;
- título;
- horas;
- Rol;
- actividad;
- notas.

Una vez realizada la migración y validada la información, la aplicación propia pasará a ser la fuente principal del registro de horas.

---

# Resultado de la evaluación

La evaluación no terminó con la elección de una herramienta comercial.

Terminó con una definición más precisa de la necesidad.

Se aprendió que:

- LAPIN necesita medir esfuerzo humano y no tiempo de actividad de la IA;
- GitHub Projects debe continuar siendo la fuente de verdad del trabajo;
- el sistema de horas debe complementar a GitHub y no duplicarlo;
- los timers generan una fricción operativa que no resulta conveniente para la forma actual de trabajo;
- la imputación manual de horas se adapta mejor al laboratorio;
- las herramientas evaluadas ofrecen más funcionalidad de la necesaria pero no resuelven exactamente el flujo requerido;
- desarrollar un sistema pequeño y específico resulta una alternativa razonable para evaluar;
- mientras ese sistema se desarrolla, Excel permite comenzar a producir información real;
- los datos registrados en Excel serán posteriormente migrados a la base de datos definitiva.

---

# Decisión

> **No adoptar de forma definitiva Toggl Track, Clockify ni Everhour para la gestión de horas de LAPIN.**

Se decide:

1. utilizar una planilla Excel como mecanismo transitorio de registro;
2. comenzar inmediatamente a generar histórico de esfuerzo humano;
3. utilizar esa experiencia como insumo para validar los requerimientos;
4. realizar el análisis funcional de una solución propia;
5. desarrollar posteriormente una aplicación local integrada con GitHub Projects;
6. migrar el histórico registrado en Excel a la base de datos del nuevo sistema.

La solución definitiva deberá mantener como principio fundamental:

> **GitHub Projects registra qué trabajo realiza LAPIN.  
> El sistema de gestión de horas registra cuánto esfuerzo humano requiere realizarlo.**