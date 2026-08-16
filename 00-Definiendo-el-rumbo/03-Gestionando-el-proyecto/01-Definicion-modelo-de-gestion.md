>**Versión:** 1.0 | 
>**Fecha:** 15/08/2026 | 
>**Autor:** Jessica
> ---

# Definición del modelo de gestión de trabajo de LAPIN

## Por qué necesitamos un sistema de gestión

A medida que LAPIN comenzó a trabajar con más especialistas aparecieron actividades simultáneas, trabajos pendientes y temas que debían retomarse días después.

Mientras el volumen era pequeño podíamos recordarlo.

A medida que LAPIN crece, necesitamos un sistema que permita entrar y responder rápidamente:

* ¿Qué estaba haciendo LAPIN?
* ¿Qué quedó a medias?
* ¿Qué Rol es responsable?
* ¿Qué está bloqueado?
* ¿Qué es prioritario?
* ¿Qué terminamos?
* ¿Cuánto trabajo produjo cada Rol?
* ¿Cuántas horas humanas requirió?

El sistema de gestión no será solamente una lista de tareas. También será parte del **registro del laboratorio**.

---

## Lo que aprendimos intentando configurar Jira

Nuestra primera búsqueda comenzó por la herramienta.

Elegimos Jira y dedicamos aproximadamente un día a intentar configurarlo para representar nuestro modelo de trabajo.

Durante ese proceso descubrimos que estábamos haciendo la pregunta equivocada.

No necesitábamos preguntarnos:

> **¿Cómo podemos adaptar LAPIN a Jira?**

Primero necesitábamos definir:

> **¿Qué necesita LAPIN de una herramienta de gestión?**

Si no definimos previamente esos requisitos podemos invertir tiempo configurando una herramienta para descubrir después que, aunque técnicamente permita hacer muchas cosas, **no representa bien nuestro modelo de trabajo**.

Por eso cambiamos el criterio:

> **Primero definimos nuestras necesidades. Después buscamos la herramienta.**

---

## La particularidad de nuestros Roles

LAPIN trabaja con especialistas que pueden ser **IA o humanos**.

Esto genera una diferencia importante respecto de un equipo tradicional: quien opera la herramienta no necesariamente es quien tiene la responsabilidad sobre el trabajo.

Una persona puede crear, modificar o cerrar una actividad mientras el responsable funcional es, por ejemplo:

`CEO`
`Knowledge & Documentation`
`UI/UX Designer`
`Sr. Developer`

Por eso necesitamos que **Rol responsable sea un dato independiente del usuario de la herramienta**.

El Rol no es simplemente una etiqueta.

Queremos utilizarlo para organizar, visualizar, filtrar y posteriormente medir el trabajo producido por nuestros distintos especialistas.

---

# Requisitos obligatorios al evaluar una herramienta

Estos puntos deben comprobarse **antes de comenzar a configurar una nueva herramienta**.

### 1. ¿Tiene campos configurables para representar nuestros Roles?

Debemos poder crear un campo estructurado como **Rol responsable**, independiente del usuario que opera el sistema.

### 2. ¿Los Roles pueden diferenciarse a simple vista?

Al mirar el tablero debemos poder reconocer rápidamente qué trabajo pertenece a cada Rol.

No queremos depender de abrir cada actividad para descubrirlo.

### 3. ¿El tablero es amigable?

Debe permitir comprender rápidamente qué trabajo existe, qué está pendiente, qué está en curso, qué está bloqueado y qué es prioritario.

La funcionalidad técnica no alcanza: **tiene que ser cómoda en el uso cotidiano**.

### 4. ¿Se puede filtrar por los campos configurables?

Especialmente necesitamos poder filtrar y, cuando sea posible, agrupar por **Rol responsable**.

Esto es necesario tanto para gestionar como para analizar posteriormente el trabajo.

### 5. ¿Tiene tags o etiquetas?

Necesitamos una clasificación flexible adicional al Rol.

El Rol responde **quién es responsable**.

Las etiquetas permiten indicar **de qué trata o con qué se relaciona** una actividad.

### 6. ¿Puede conectarse con ChatGPT?

La integración no tiene que existir desde el primer día, pero debemos evaluar si la herramienta permite una futura automatización con ChatGPT mediante API, integraciones u otros mecanismos razonables.

El objetivo futuro es reducir progresivamente la operación manual del sistema.

### 7. ¿Puede relacionarse con una herramienta de registro de horas?

Necesitamos registrar **horas humanas** para conocer cuánto esfuerzo humano requiere producir los resultados de LAPIN.

El time tracking puede pertenecer a la misma herramienta o resolverse mediante una solución externa, siempre que ambas puedan relacionarse de forma práctica.

---

## Otros criterios importantes

Además de los requisitos anteriores, debemos observar:

* gestión de backlog;
* estados y workflow;
* prioridad;
* estimación del trabajo;
* métricas;
* trazabilidad mediante fechas;
* posibilidad de relacionar una actividad con su resultado o evidencia;
* costo sostenible;
* baja fricción operativa.

Una herramienta muy completa puede igualmente ser descartada si mantenerla requiere demasiado trabajo.

> **El sistema tiene que reducir nuestra carga de gestión, no convertirse en otra cosa que tengamos que gestionar.**

---

## Registrar resultados, no clics

El sistema debe registrar **unidades de trabajo con resultados identificables**.

No necesitamos crear una actividad por cada campo creado, configuración modificada o acción ejecutada.

Nos interesa poder relacionar:

**Actividad → Rol responsable → Resultado → Fechas → Estimación → Horas humanas → Evidencia**

Esto permitirá reconstruir qué produjo LAPIN y cuánto esfuerzo requirió.

---

## Sistema de registro de horas

El registro de horas humanas es complementario al sistema de gestión.

No buscamos medir cuánto tiempo “trabajó una IA”.

Nos interesa conocer **cuánta intervención humana necesitó LAPIN para producir sus resultados**.

Con el tiempo esto permitirá analizar si el modelo realmente reduce trabajo humano, dónde requiere mayor intervención y cómo evoluciona esa relación.

---

## Criterio para la próxima búsqueda

A partir de la experiencia con Jira no comenzaremos una nueva evaluación intentando configurar cada herramienta.

Primero comprobaremos los **siete requisitos obligatorios**.

Si una herramienta falla en un requisito crítico para nuestro modelo, podremos descartarla antes de invertir tiempo en configurarla.

Las herramientas que superen ese primer filtro podrán pasar a una prueba real de uso.

> **No buscamos la herramienta de gestión más completa. Buscamos la que mejor represente el modelo de trabajo de LAPIN con la menor fricción posible.**
