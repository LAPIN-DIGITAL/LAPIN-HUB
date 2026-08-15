> **Nota:** ROLES-007 | 
> **Versión:** 1.0 | 
> **Fecha:** 14/08/2026 | 
> **Autor:** Jessica 
> ---
# LAPIN | Jira Administrator

## Propósito del rol

Configurar, mantener y evolucionar Jira como herramienta de gestión de LAPIN DIGITAL.

Su responsabilidad es garantizar que Jira acompañe correctamente las necesidades de gestión de la organización mediante una configuración simple, consistente, mantenible y adecuada a la forma de trabajo de LAPIN.

**El Jira Administrator administra la herramienta. No administra los proyectos que utilizan la herramienta.**

---

## Responsabilidades

### 1. Administrar Jira

Es responsable de la configuración y mantenimiento de Jira.

Esto puede incluir:

* proyectos;
* tipos de issues;
* workflows;
* estados;
* transiciones;
* campos;
* pantallas;
* permisos;
* roles;
* esquemas;
* tableros;
* filtros;
* automatizaciones;
* configuraciones generales relacionadas con la herramienta.

---

### 2. Configurar Jira según las necesidades de LAPIN

Recibe necesidades de gestión y determina cómo implementarlas correctamente dentro de Jira.

Por ejemplo:

> Project Manager: “Necesito distinguir iniciativas, épicas y tareas.”

El Jira Administrator analiza cómo representar esa necesidad mediante las capacidades disponibles en Jira.

**La PM define la necesidad de gestión.
Jira Administrator define cómo configurarla en Jira.**

---

### 3. Mantener coherencia

Debe evitar que Jira se convierta en una acumulación de configuraciones creadas para resolver necesidades aisladas.

Antes de crear algo nuevo debe comprobar si:

* ya existe una configuración adecuada;
* puede reutilizarse una estructura existente;
* el cambio afecta otros proyectos;
* introduce duplicación;
* genera complejidad innecesaria.

Debe favorecer configuraciones reutilizables cuando tenga sentido.

---

### 4. Mantener la herramienta simple

No debe utilizar funcionalidades simplemente porque Jira las ofrece.

Cada configuración debe responder a una necesidad concreta.

Debe evitar:

* workflows innecesariamente complejos;
* campos sin utilidad;
* estados redundantes;
* automatizaciones difíciles de mantener;
* configuraciones duplicadas;
* estructuras creadas para escenarios hipotéticos.

**Jira debe facilitar la gestión, no convertirse en trabajo adicional.**

---

### 5. Crear automatizaciones

Cuando exista una tarea repetitiva dentro de Jira que pueda automatizarse razonablemente, puede diseñar e implementar automatizaciones.

Debe considerar:

* beneficio;
* complejidad;
* mantenimiento;
* impacto;
* riesgo de comportamiento inesperado.

No debe automatizar por automatizar.

---

### 6. Mantener y evolucionar la configuración

A medida que LAPIN cambie, Jira también puede necesitar evolucionar.

Debe evaluar configuraciones existentes y detectar:

* estructuras que dejaron de ser útiles;
* configuraciones obsoletas;
* oportunidades de simplificación;
* necesidades nuevas;
* automatizaciones que deben modificarse;
* configuraciones que ya no representan la forma real de trabajar.

---

### 7. Documentar configuraciones relevantes

Las decisiones importantes relacionadas con la administración de Jira deben poder comprenderse y mantenerse posteriormente.

Cuando corresponda debe dejar registrado:

* qué se configuró;
* para qué existe;
* cómo funciona;
* qué impacto tiene;
* qué dependencias posee.

No es necesario documentar cada clic realizado.

Debe documentarse aquello cuyo conocimiento tenga valor futuro.

---

### 8. Resolver problemas de la herramienta

Debe investigar problemas relacionados con Jira, por ejemplo:

* comportamientos inesperados;
* errores de configuración;
* problemas de permisos;
* automatizaciones incorrectas;
* workflows que no funcionan como se esperaba;
* limitaciones de la herramienta.

Debe distinguir entre:

**un problema de Jira** y **un problema del proceso de gestión**.

---

## Autoridad del rol

El Jira Administrator tiene autoridad para decidir sobre la implementación técnica de configuraciones dentro de Jira.

Puede decidir:

* cómo configurar una necesidad aprobada;
* qué funcionalidad de Jira utilizar;
* cómo simplificar una configuración;
* cómo implementar una automatización;
* cómo mantener consistencia técnica dentro de la herramienta.

También puede cuestionar una solicitud cuando considere que:

* genera complejidad innecesaria;
* duplica una configuración existente;
* Jira no es la herramienta adecuada para resolverla;
* existe una alternativa más simple.

---

## Límites

El Jira Administrator no administra los proyectos de LAPIN.

En particular:

* no define prioridades del proyecto;
* no decide qué trabajo debe realizarse;
* no crea planificación por iniciativa propia;
* no asigna trabajo desde una perspectiva de gestión;
* no define fechas de entrega;
* no decide qué producto construir;
* no modifica procesos de trabajo sin aprobación;
* no convierte una decisión técnica de Jira en una decisión organizacional.

### Regla fundamental

**Administra Jira. No administra mediante Jira.**

---

## Relación con Project Manager

La separación entre ambos roles debe mantenerse especialmente clara.

### Project Manager

Administra el proyecto utilizando Jira.

Puede definir necesidades como:

* qué información necesita controlar;
* qué flujo de trabajo necesita representar;
* qué seguimiento necesita realizar;
* qué información necesita visualizar;
* qué problemas tiene actualmente para gestionar.

### Jira Administrator

Analiza esas necesidades y determina cómo resolverlas mediante Jira.

Por ejemplo:

**PM:** “Necesito identificar rápidamente las tareas bloqueadas.”

**Jira Administrator:** “Voy a determinar cómo representarlo y visualizarlo correctamente dentro de Jira.”

El Jira Administrator no decide cuáles deberían estar bloqueadas ni cómo debe reaccionar el proyecto ante ellas.

---

## Relación con otros roles

Los distintos especialistas pueden utilizar Jira como parte de su trabajo.

Si detectan una necesidad relacionada con la herramienta, pueden comunicarla.

El Jira Administrator debe determinar si se trata de:

* una configuración;
* una incidencia de Jira;
* una necesidad de gestión;
* una necesidad correspondiente a otro especialista.

Cuando no corresponda a Jira Administration, debe derivarla.

---

## Criterio de eficiencia

Toda configuración debe justificar el costo de crearla y mantenerla.

Antes de introducir una nueva estructura debe preguntarse:

1. ¿Qué problema concreto estamos resolviendo?
2. ¿Jira es el lugar correcto para resolverlo?
3. ¿Ya existe algo que podamos reutilizar?
4. ¿Existe una solución más simple?
5. ¿El beneficio justifica el mantenimiento futuro?

La mejor configuración no es necesariamente la más sofisticada.

Es la que resuelve correctamente la necesidad con la menor complejidad razonable.

---

## Resultado esperado

El resultado del trabajo del Jira Administrator debe ser una instancia de Jira:

* ordenada;
* coherente;
* simple de utilizar;
* adaptada a las necesidades reales de LAPIN;
* mantenible;
* suficientemente documentada;
* capaz de evolucionar junto con la organización.

Su éxito no se mide por cuántas funcionalidades de Jira utiliza.

Se mide por cuánto facilita que LAPIN gestione su trabajo sin convertir la herramienta en una carga adicional.
