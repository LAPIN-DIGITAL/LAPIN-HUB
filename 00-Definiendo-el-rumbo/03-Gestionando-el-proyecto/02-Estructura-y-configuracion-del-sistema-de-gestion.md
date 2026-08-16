> **Versión:** 1.1
> **Fecha:** 15/08/2026
> **Autor:** Jessica

# LAPIN | Estructura y configuración del sistema de gestión

## Propósito

Definir la estructura estándar utilizada por LAPIN DIGITAL para organizar, visualizar y registrar su trabajo.

Este documento no describe solamente cómo utilizar una herramienta específica.

Define **cómo debe funcionar el sistema de gestión de LAPIN**, independientemente de la plataforma utilizada para implementarlo.

Actualmente el modelo se encuentra implementado mediante **GitHub Projects**.

---

# 1. Principio de independencia de la herramienta

La estructura de gestión pertenece al modelo organizacional de LAPIN y no a la herramienta utilizada para implementarla.

Si en el futuro se reemplaza la herramienta de gestión, deberán preservarse, siempre que sea técnicamente posible:

* conceptos;
* nomenclaturas;
* campos;
* significados;
* relaciones;
* reglas;
* criterios de visualización;
* criterios de medición.

La herramienta debe adaptarse al modelo de LAPIN.

> **El modelo no debe modificarse únicamente para adaptarse a una herramienta.**

Esto permite mantener una forma de trabajo consistente aunque cambie la tecnología utilizada.

---

# 2. Qué representa una actividad

El sistema de gestión no funciona únicamente como una lista de tareas pendientes.

También forma parte del registro del laboratorio.

> **Una actividad representa trabajo del laboratorio que produce conocimiento o un resultado verificable.**

Por este motivo no se crean actividades para representar cada acción administrativa realizada durante el trabajo.

Por ejemplo:

* crear un campo;
* cambiar un color;
* modificar una opción;
* realizar una configuración menor;

pueden formar parte de una actividad mayor, pero no constituyen necesariamente actividades independientes.

Una actividad debe permitir posteriormente comprender:

* qué se buscaba realizar;
* por qué se realizó;
* qué Rol fue responsable;
* qué resultado se obtuvo;
* qué evidencia dejó;
* cuándo ocurrió;
* cuánto trabajo representó;
* cuánto esfuerzo humano requirió, cuando corresponda.

---

# 3. Estructura estándar de una actividad

Las actividades pueden utilizar los siguientes datos:

| Campo                     | Propósito                                                                       |
| ------------------------- | ------------------------------------------------------------------------------- |
| **Título**                | Identificar claramente la actividad.                                            |
| **Description**           | Explicar qué debe realizarse y qué resultado se espera obtener.                 |
| **Activity Type**         | Identificar estructuralmente si la actividad es `EPIC`, `USER STORY` o `TASK`.  |
| **Rol responsable**       | Identificar el Rol de LAPIN responsable funcionalmente del trabajo.             |
| **Status**                | Representar la situación actual de la actividad.                                |
| **Priority**              | Indicar la prioridad relativa.                                                  |
| **Estimate**              | Representar mediante Story Points el tamaño o complejidad relativa del trabajo. |
| **Iteration**             | Identificar el período de trabajo al que pertenece.                             |
| **Created**               | Registrar cuándo fue creada.                                                    |
| **Start Date**            | Registrar cuándo comenzó efectivamente el trabajo.                              |
| **Updated**               | Registrar la última actualización.                                              |
| **Due Date**              | Registrar cuándo se espera finalizar.                                           |
| **Finish Date**           | Registrar cuándo finalizó efectivamente.                                        |
| **Labels**                | Incorporar señales o clasificaciones adicionales cuando sean necesarias.        |
| **Resultado / evidencia** | Permitir identificar y localizar el resultado producido por la actividad.       |

No todos los campos necesitan utilizarse en todas las actividades.

Debe evitarse completar información que no aporte valor únicamente por mantener una formalidad administrativa.

---

# 4. Tipos de actividad

`Activity Type` identifica qué representa una actividad dentro de la estructura de trabajo.

Los valores actuales son:

| Activity Type  | Propósito                                                                     |
| -------------- | ----------------------------------------------------------------------------- |
| **EPIC**       | Contenedor de un objetivo o conjunto de resultados relacionados.              |
| **USER STORY** | Unidad principal de trabajo gestionable que produce un resultado verificable. |
| **TASK**       | Parte de una User Story que necesita seguimiento independiente.               |

El tipo de actividad debe existir como **dato estructurado**.

Puede utilizarse una nomenclatura visible en el título, por ejemplo:

`EPIC — Sistema de gestión de trabajo de LAPIN`

pero el sistema no debe depender del texto del título para determinar qué tipo de actividad representa.

Esto permite utilizar `Activity Type` posteriormente para:

* filtros;
* vistas;
* agrupaciones;
* métricas;
* automatizaciones.

---

# 5. Jerarquía de actividades

La jerarquía estándar de LAPIN es:

`EPIC → USER STORY → TASK`

## EPIC

Una Epic representa un objetivo o agrupación superior.

Puede contener diferentes resultados relacionados con un mismo objetivo.

Funciona principalmente como contenedor y no necesariamente representa trabajo ejecutable directamente.

## USER STORY

La User Story constituye la **unidad principal de trabajo del laboratorio**.

Debe perseguir un resultado suficientemente identificable y verificable como para que tenga sentido registrar que fue realizado.

## TASK

Una Task representa una parte del trabajo necesario para completar una User Story cuando esa parte necesita seguimiento independiente.

> **No toda User Story necesita Tasks.**

Si algo representa solamente un paso menor necesario para completar una User Story, permanece dentro de ella.

Si necesita su propio estado, seguimiento o gestión, puede convertirse en Task.

Esto evita transformar el sistema en un registro de microacciones.

---

# 6. Relaciones entre actividades

La jerarquía debe mantenerse mediante relaciones estructuradas `Parent / Sub-issue` o mediante el mecanismo equivalente disponible en la herramienta utilizada.

Ejemplo:

```text
EPIC
└── USER STORY
    └── TASK
```

Cada actividad mantiene su propio identificador.

Por ejemplo:

`#16 → #11 → #17`

Los identificadores permiten establecer relaciones inequívocas sin depender exclusivamente del texto de los títulos.

Esto resulta especialmente importante para futuras integraciones y automatizaciones.

> **Cuando exista un identificador o relación estructurada, una automatización debe utilizarlo antes que intentar deducir relaciones interpretando texto.**

---

# 7. Rol responsable

## Concepto

El trabajo de LAPIN se organiza mediante **roles especializados que pueden ser desempeñados por IA o por personas**.

Estos roles no necesariamente poseen:

* usuario;
* contraseña;
* cuenta propia en la herramienta;
* identidad técnica equivalente a una persona física.

Por este motivo:

> **Quien opera la herramienta no necesariamente es quien tiene la responsabilidad sobre el trabajo.**

Una persona puede crear, modificar, mover o cerrar manualmente una actividad mientras la responsabilidad funcional pertenece a un Rol de LAPIN.

Por lo tanto, `Rol responsable` debe existir como un **dato estructurado independiente del usuario o Assignee de la herramienta**.

El Rol responsable constituye una de las dimensiones centrales del sistema de gestión.

Debe permitir identificar, filtrar, agrupar y posteriormente medir el trabajo realizado por los distintos especialistas de LAPIN.

## Nomenclatura

Los Roles utilizan los **códigos organizacionales oficiales definidos por Recursos Humanos**.

Estos códigos deben reutilizarse en todos los sistemas donde sea necesario representar un Rol.

No deben crearse abreviaturas alternativas dentro de la herramienta de gestión.

Formato general:

`LD-[CÓDIGO DE ROL]`

La fuente oficial para determinar los códigos válidos corresponde a la documentación de Recursos Humanos.

## Representación visual

Cada Rol responsable utiliza un color que permita diferenciarlo rápidamente de otros Roles.

El objetivo del color es facilitar la lectura del tablero y reconocer visualmente la distribución del trabajo.

---

# 8. Estados

Los estados estándar son:

| Status          | Descripción                                                                                  |
| --------------- | -------------------------------------------------------------------------------------------- |
| **BACKLOG**     | Trabajo identificado que todavía no fue seleccionado para realizarse.                        |
| **TO DO**       | Trabajo priorizado y seleccionado para realizarse en el período actual.                      |
| **IN PROGRESS** | Trabajo que se encuentra actualmente en ejecución por el Rol responsable.                    |
| **BLOCKED**     | Trabajo que no puede continuar temporalmente por una dependencia, información o impedimento. |
| **IN REVIEW**   | Trabajo realizado pendiente de revisión, validación o aprobación.                            |
| **DONE**        | Trabajo finalizado y considerado completo.                                                   |

---

# 9. Flujo de trabajo

El flujo principal es:

`BACKLOG → TO DO → IN PROGRESS → IN REVIEW → DONE`

`BLOCKED` representa una interrupción temporal del trabajo.

Flujo habitual:

`IN PROGRESS → BLOCKED → IN PROGRESS`

Una actividad en `IN REVIEW` puede regresar a `IN PROGRESS` cuando la revisión determine que necesita trabajo adicional.

Durante una instancia de planificación, una actividad que pierda prioridad puede regresar a `BACKLOG`.

El sistema debe mantener suficiente flexibilidad para mover actividades cuando la realidad del trabajo lo requiera.

---

# 10. Prioridad

La prioridad se representa mediante un campo estructurado.

Los valores y colores estándar son:

| Priority   | Color   | Significado                          |
| ---------- | ------- | ------------------------------------ |
| **URGENT** | Rojo    | Requiere atención inmediata.         |
| **HIGH**   | Naranja | Alta prioridad.                      |
| **MEDIUM** | Verde   | Prioridad normal.                    |
| **LOW**    | Azul    | Puede esperar sin impacto relevante. |

La prioridad debe poder identificarse rápidamente desde la visualización del trabajo.

No debe duplicarse mediante Labels.

---

# 11. Fechas

LAPIN utiliza cinco fechas principales para mantener trazabilidad temporal:

| Campo           | Significado                                     |
| --------------- | ----------------------------------------------- |
| **Created**     | Fecha en que fue creada la actividad.           |
| **Start Date**  | Fecha en que comenzó efectivamente el trabajo.  |
| **Updated**     | Fecha de la última actualización.               |
| **Due Date**    | Fecha prevista para finalizar la actividad.     |
| **Finish Date** | Fecha en que el trabajo finalizó efectivamente. |

Es importante mantener las diferencias conceptuales:

> **Created ≠ Start Date**

Una actividad puede existir durante un período en `BACKLOG` antes de comenzar a trabajarse.

> **Due Date ≠ Finish Date**

`Due Date` representa cuándo se esperaba finalizar.

`Finish Date` representa cuándo finalizó realmente.

La herramienta utilizada puede generar adicionalmente fechas técnicas, como el momento de cierre de un Issue.

Estas fechas pueden conservarse como información complementaria, pero no deben confundirse con las fechas operativas definidas por LAPIN.

---

# 12. Estimación

`Estimate` representa el **tamaño o complejidad relativa de una actividad**, utilizando **Story Points**.

Los Story Points no representan horas ni una duración exacta.

Permiten comparar una actividad con otra considerando conjuntamente aspectos como:

* complejidad;
* volumen de trabajo;
* incertidumbre.

LAPIN utiliza una escala basada en **Fibonacci**:

`1 · 2 · 3 · 5 · 8 · 13`

La separación entre valores aumenta junto con el tamaño de la actividad porque cuanto mayor es el trabajo, menor es la precisión con la que puede estimarse.

| Story Points | Interpretación                       |
| ------------ | ------------------------------------ |
| **1**        | Mínimo                               |
| **2**        | Pequeño                              |
| **3**        | Medio                                |
| **5**        | Considerable                         |
| **8**        | Grande                               |
| **13**       | Muy grande; evaluar posible división |

La estimación es relativa.

Una actividad de `5` no significa cinco horas. Representa mayor esfuerzo, complejidad o incertidumbre que una actividad estimada en `2` o `3`.

> **Story Points ≠ horas humanas**

Aunque la herramienta permita técnicamente ingresar otros números, los valores válidos para LAPIN son:

`1 · 2 · 3 · 5 · 8 · 13`

Las horas humanas constituyen otra dimensión y se registran mediante el sistema de **time tracking**.

Mantener ambas medidas separadas permitirá posteriormente comparar:

**tamaño estimado del trabajo → horas humanas realmente requeridas**

---

# 13. Iteraciones

`Iteration` permite agrupar actividades dentro de períodos de trabajo determinados.

Su propósito es permitir posteriormente analizar:

* trabajo iniciado;
* trabajo terminado;
* producción por período;
* producción por Rol;
* trabajo pendiente;
* evolución de la capacidad del sistema.

La configuración temporal de las iteraciones deberá mantenerse consistente con el período de medición utilizado por LAPIN.

---

# 14. Labels

Los Labels funcionan como **señales adicionales o ayudas memoria**.

No constituyen el mecanismo principal de clasificación.

## Reglas

Los Labels:

* se crean únicamente cuando existe una necesidad concreta;
* utilizan nombres breves;
* deben aportar información adicional;
* no deben duplicar información existente;
* no reemplazan `Rol responsable`;
* no reemplazan `Priority`;
* no reemplazan `Status`;
* no reemplazan `Activity Type`.

No se crean Labels preventivamente para escenarios hipotéticos.

## Color

Todos los Labels utilizados por LAPIN se normalizan utilizando:

**Color: amarillo**

Esto permite identificarlos visualmente como información complementaria sin competir con los colores utilizados para Roles o Prioridades.

---

# 15. Estructura y visualización

La estructura de las actividades y su visualización son conceptos diferentes.

Una `EPIC`, una `USER STORY` y una `TASK` pueden pertenecer al mismo sistema sin necesidad de aparecer simultáneamente en el mismo tablero.

Esto permite mantener **una única fuente de información** y construir diferentes vistas sobre ella.

> **Que una actividad no aparezca en una vista no significa que esté fuera del sistema.**

La relación jerárquica entre actividades debe mantenerse independientemente de la vista utilizada para observarlas.

---

# 16. Vistas

El sistema puede utilizar múltiples vistas sobre las mismas actividades.

Las vistas se crean cuando responden a una necesidad concreta de gestión.

No se crean preventivamente.

## Vista operativa

Está destinada al seguimiento cotidiano.

Puede mostrar principalmente:

* `USER STORY`;
* `TASK`, cuando requiera gestión independiente.

Las `EPIC` pueden excluirse para evitar mezclar contenedores de objetivos con trabajo ejecutable.

## Vista de EPICS

Permite visualizar exclusivamente:

`Activity Type = EPIC`

Su objetivo es proporcionar una visión de los grandes objetivos y agrupaciones de trabajo sin interferir con el tablero operativo.

## Otras vistas

Cuando exista una necesidad real pueden crearse vistas específicas por:

* Activity Type;
* Rol responsable;
* Iteration;
* proyecto;
* producto;
* otros datos estructurados existentes.

> **Una vista existe porque responde una pregunta de gestión.**

La cantidad de vistas no constituye un objetivo.

---

# 17. Visualización del Board

El Board constituye una herramienta de supervisión y no solamente una representación estética del trabajo.

Debe permitir comprender rápidamente:

* cuánto trabajo existe;
* qué está pendiente;
* qué está en ejecución;
* qué está bloqueado;
* qué necesita revisión;
* qué es prioritario;
* qué Rol es responsable.

Las tarjetas deben mantenerse suficientemente compactas para visualizar varias actividades simultáneamente.

Como criterio visual:

| Elemento            | Representación                                      |
| ------------------- | --------------------------------------------------- |
| **Status**          | Posición de la tarjeta                              |
| **Rol responsable** | Código corto + color                                |
| **Priority**        | Color                                               |
| **Labels**          | Amarillo                                            |
| **Fechas**          | Visibles únicamente cuando aportan información útil |

Los colores transmiten información y no se utilizan únicamente con fines decorativos.

Debe evitarse mostrar información redundante que aumente innecesariamente el tamaño o ruido visual de las tarjetas.

---

# 18. Descripciones de Status

Las descripciones de los Status deben conservarse en la documentación del sistema.

No necesitan mostrarse permanentemente dentro del Board cuando su visualización perjudique la usabilidad.

Durante la implementación actual se comprobó que las descripciones visibles consumían una cantidad significativa de espacio vertical en los encabezados de las columnas.

Por este motivo fueron eliminadas de la interfaz operativa.

Los estados continúan siendo:

`BACKLOG · TO DO · IN PROGRESS · BLOCKED · IN REVIEW · DONE`

y su significado permanece definido formalmente en este documento.

> **La documentación conserva el conocimiento. El tablero prioriza la operación.**

No es necesario duplicar permanentemente en la interfaz información formalmente documentada cuando esa duplicación perjudica la lectura del trabajo.

---

# 19. Backlog

`BACKLOG` contiene trabajo identificado que todavía no fue seleccionado para ejecución.

Su función es proporcionar una vista rápida del trabajo disponible para futuras instancias de planificación.

Una actividad puede regresar al `BACKLOG` cuando deja de estar priorizada para el período actual.

El Backlog no representa trabajo abandonado.

Representa **trabajo conocido que todavía no corresponde ejecutar**.

---

# 20. Resultado y evidencia

Toda actividad debe producir un resultado identificable.

El resultado puede consistir, según el tipo de trabajo, en:

* documentación;
* código;
* diseño;
* configuración;
* análisis;
* decisión;
* investigación;
* implementación;
* conocimiento obtenido mediante un experimento;
* otro entregable verificable.

Cuando corresponda, la actividad deberá permitir localizar la evidencia producida.

Esto permite relacionar el sistema de gestión con la trazabilidad histórica del laboratorio.

---

# 21. Time tracking

El tamaño estimado del trabajo y el tiempo humano invertido representan dimensiones diferentes.

Por este motivo:

**Estimate → tamaño/complejidad relativa del trabajo**

**Time tracking → esfuerzo humano invertido**

El sistema de gestión debe permitir relacionar una actividad con el registro de tiempo correspondiente.

El time tracking puede implementarse mediante una herramienta independiente siempre que mantenga una relación clara con las actividades gestionadas.

Esta información permitirá analizar cuánto esfuerzo humano requiere producir los distintos resultados de LAPIN y cómo evoluciona esa relación.

La implementación concreta del sistema de time tracking se documentará de forma independiente.

---

# 22. Escalabilidad

La separación entre **datos estructurados y vistas** permite que el modelo pueda crecer sin necesidad de crear sistemas de gestión aislados para cada nueva línea de trabajo.

Las actividades pueden continuar utilizando los mismos conceptos:

* Activity Type;
* Rol responsable;
* Status;
* Priority;
* Estimate;
* Iteration;
* fechas;
* Labels;
* relaciones Parent / Sub-issue.

Si LAPIN incorpora distintos proyectos, productos o líneas de trabajo y aparece una necesidad real de distinguirlos formalmente, podrá incorporarse un dato estructurado específico para representar esa pertenencia.

No debe crearse preventivamente mientras no exista esa necesidad.

> **La estructura crece cuando aparece una necesidad real, no cuando imaginamos que algún día podría necesitarse.**

---

# 23. Baja fricción operativa

Mantener actualizado el sistema no debe convertirse en una actividad administrativa desproporcionada.

La información registrada debe justificar el esfuerzo necesario para mantenerla.

Por este motivo:

* no se crean campos sin necesidad;
* no se crean Labels preventivamente;
* no se crean Tasks para microacciones;
* no se registran microacciones como actividades independientes;
* no se crean vistas sin una necesidad concreta;
* se priorizan datos estructurados que puedan reutilizarse;
* se favorece la carga rápida;
* se evita duplicar información;
* se mantiene el Board visualmente compacto.

> **Mantener el sistema no debe convertirse en el trabajo.**

---

# 24. Preparación para automatización

La estructura se define de forma suficientemente precisa para ser interpretada posteriormente tanto por personas como por sistemas automatizados.

Una futura IA que opere el sistema no deberá decidir libremente:

* qué tipos de actividad existen;
* qué significa una Epic;
* qué significa una User Story;
* cuándo corresponde crear una Task;
* cómo establecer relaciones jerárquicas;
* qué significa un Rol;
* cómo nombrarlo;
* qué Status existen;
* qué prioridades existen;
* qué representan las fechas;
* cuándo crear un Label;
* qué significa Estimate;
* qué valores de Story Points son válidos;
* cómo interpretar una actividad.

Debe utilizar las reglas y nomenclaturas definidas por LAPIN.

Las automatizaciones deben utilizar preferentemente:

* campos estructurados;
* identificadores;
* relaciones Parent / Sub-issue;
* valores normalizados.

No deben intentar reconstruir información mediante interpretación de títulos cuando existe una fuente estructurada disponible.

Por ejemplo:

> `Activity Type` determina estructuralmente si una actividad es `EPIC`, `USER STORY` o `TASK`. El prefijo escrito en el título puede facilitar la lectura humana, pero no debe ser utilizado como fuente principal por una automatización.

Del mismo modo:

> `Rol responsable` representa la responsabilidad funcional sobre la actividad, utiliza los códigos oficiales definidos por Recursos Humanos y nunca debe confundirse con el usuario que opera la herramienta.

La automatización debe implementar el modelo.

> **No debe reinterpretarlo.**

---

# 25. Implementación actual

La primera implementación del sistema de gestión se realizó sobre **Jira**.

La experiencia permitió detectar que la herramienta no se adaptaba de forma suficientemente práctica al modelo que LAPIN necesitaba implementar.

Ese experimento llevó a definir con mayor precisión los requisitos del sistema antes de seleccionar una nueva herramienta.

Actualmente el modelo se encuentra implementado mediante **GitHub Projects**, que se ajusta mejor a la estructura definida por LAPIN.

La estructura fue validada utilizando actividades reales y actualmente permite:

* utilizar `Activity Type` como dato estructurado;
* mantener la jerarquía `EPIC → USER STORY → TASK`;
* relacionar actividades mediante Parent / Sub-issue;
* conservar identificadores individuales;
* incorporar las actividades al mismo Project;
* separar visualmente distintos tipos de actividad mediante vistas;
* mantener las EPICS fuera del Board operativo;
* visualizar independientemente diferentes Activity Types;
* filtrar utilizando datos estructurados;
* mantener un Board compacto orientado al trabajo cotidiano.

La implementación actual utiliza:

| Concepto LAPIN          | Implementación actual                                         |
| ----------------------- | ------------------------------------------------------------- |
| Activity Type           | Campo personalizado de selección única                        |
| Rol responsable         | Campo personalizado                                           |
| Status                  | Campo de estado / columnas del Board                          |
| Priority                | Campo personalizado                                           |
| Estimate                | Campo numérico limitado conceptualmente a `1, 2, 3, 5, 8, 13` |
| Iteration               | Campo de iteración                                            |
| Start Date              | Campo de fecha                                                |
| Due Date                | Campo de fecha                                                |
| Finish Date             | Campo de fecha                                                |
| Created / Updated       | Información temporal de GitHub                                |
| Labels                  | Labels de GitHub                                              |
| Jerarquía               | Issues / Parent / Sub-issues                                  |
| Identificación          | ID individual de cada Issue                                   |
| Visualización operativa | GitHub Projects Board                                         |
| Vistas adicionales      | Vistas filtradas del mismo GitHub Project                     |

Actualmente `Activity Type` utiliza los siguientes valores:

`EPIC · USER STORY · TASK`

En la implementación actual mediante una cuenta personal, este campo permite mantener el tipo de actividad como información estructurada independientemente de las convenciones utilizadas en los títulos.

Si en el futuro la herramienta cambia o aparecen mecanismos estructurados más adecuados, la implementación podrá evolucionar manteniendo **el significado del modelo**.

---

# Resultado

LAPIN cuenta con una estructura estándar para gestionar su trabajo independientemente de la herramienta utilizada.

El modelo define:

* qué representa una actividad;
* qué tipos de actividad existen;
* cómo se organiza la jerarquía;
* cómo se relacionan las actividades;
* cómo se atribuye la responsabilidad;
* cómo se organiza el flujo;
* cómo se representa la prioridad;
* qué fechas se utilizan;
* cómo se estima el trabajo;
* cómo se organizan períodos;
* cómo se utilizan Labels;
* cómo se construyen vistas;
* cómo debe visualizarse el trabajo;
* cómo se conserva evidencia;
* cómo se relacionará el esfuerzo humano;
* cómo puede escalar la estructura;
* cómo se prepara la información para medición y futura automatización.

Actualmente este modelo se encuentra implementado mediante **GitHub Projects**.

La implementación concreta puede evolucionar.

Los principios, significados y reglas definidos en este documento constituyen la referencia para mantener consistente el sistema de gestión de LAPIN aunque cambien las herramientas utilizadas.
