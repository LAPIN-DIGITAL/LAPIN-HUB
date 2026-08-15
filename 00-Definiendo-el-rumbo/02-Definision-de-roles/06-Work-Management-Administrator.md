> **Código:** LD-WMAdm |  
> **Versión:** 2.0 |  
> **Fecha:** 15/08/2026 |  
> **Autor:** Jessica  
> ---

# LAPIN | Work Management Administrator

## Propósito del rol

Configurar, mantener y evolucionar el sistema y las herramientas utilizadas para la gestión del trabajo de LAPIN DIGITAL.

Su responsabilidad es garantizar que la herramienta de gestión acompañe correctamente las necesidades de la organización mediante una configuración simple, consistente, mantenible y adecuada a la forma de trabajo de LAPIN.

Actualmente LAPIN utiliza **GitHub Projects** como herramienta de gestión, pero el rol no depende de una herramienta específica.

**El Work Management Administrator administra la herramienta de gestión. No administra los proyectos que utilizan la herramienta.**

---

## Responsabilidades

### 1. Administrar la herramienta de gestión

Es responsable de configurar y mantener la herramienta utilizada por LAPIN para gestionar el trabajo.

Esto puede incluir:

- proyectos;
- campos;
- estados;
- vistas;
- filtros;
- iteraciones;
- etiquetas;
- tipos de elementos;
- permisos;
- automatizaciones;
- configuraciones relacionadas con la gestión del trabajo.

---

### 2. Configurar la herramienta según las necesidades de LAPIN

Recibe necesidades de gestión y determina cómo implementarlas correctamente utilizando las capacidades disponibles en la herramienta.

Por ejemplo:

> Project Manager: “Necesito identificar rápidamente qué tareas están bloqueadas.”

El Work Management Administrator determina cómo representar y visualizar esa necesidad dentro de la herramienta.

**La PM define la necesidad de gestión.  
Work Management Administrator define cómo implementarla en la herramienta.**

---

### 3. Mantener coherencia

Debe evitar que el sistema de gestión se convierta en una acumulación de configuraciones creadas para resolver necesidades aisladas.

Antes de crear algo nuevo debe comprobar si:

- ya existe una configuración adecuada;
- puede reutilizarse una estructura existente;
- el cambio afecta otros proyectos;
- introduce duplicación;
- genera complejidad innecesaria.

Debe favorecer configuraciones reutilizables cuando tenga sentido.

---

### 4. Mantener la herramienta simple

No debe utilizar funcionalidades simplemente porque la herramienta las ofrece.

Cada configuración debe responder a una necesidad concreta.

Debe evitar:

- campos sin utilidad;
- estados redundantes;
- vistas innecesarias;
- automatizaciones difíciles de mantener;
- configuraciones duplicadas;
- estructuras creadas para escenarios hipotéticos.

**La herramienta debe facilitar la gestión, no convertirse en trabajo adicional.**

---

### 5. Crear automatizaciones

Cuando exista una tarea repetitiva dentro del sistema de gestión que pueda automatizarse razonablemente, puede diseñar e implementar automatizaciones.

Debe considerar:

- beneficio;
- complejidad;
- mantenimiento;
- impacto;
- riesgo de comportamiento inesperado.

No debe automatizar por automatizar.

---

### 6. Mantener y evolucionar la configuración

A medida que LAPIN cambie, su sistema de gestión también puede necesitar evolucionar.

Debe detectar:

- estructuras que dejaron de ser útiles;
- configuraciones obsoletas;
- oportunidades de simplificación;
- necesidades nuevas;
- automatizaciones que deben modificarse;
- configuraciones que ya no representan la forma real de trabajar.

---

### 7. Evaluar las capacidades y limitaciones de la herramienta

Debe conocer las posibilidades y limitaciones de la herramienta utilizada.

Cuando una necesidad no pueda resolverse adecuadamente debe determinar si:

- existe una alternativa dentro de la herramienta;
- puede resolverse mediante automatización o integración;
- requiere complementar la herramienta;
- la limitación debe aceptarse;
- la herramienta dejó de ser adecuada para la necesidad de LAPIN.

Debe comunicar estas situaciones a la PM para que pueda tomarse la decisión correspondiente.

---

### 8. Documentar configuraciones relevantes

Las configuraciones importantes deben poder comprenderse y mantenerse posteriormente.

Cuando corresponda debe dejar registrado:

- qué se configuró;
- para qué existe;
- cómo funciona;
- qué impacto tiene;
- qué dependencias posee.

No es necesario documentar cada acción realizada.

Debe documentarse aquello cuyo conocimiento tenga valor futuro.

---

### 9. Resolver problemas de la herramienta

Debe investigar problemas relacionados con el sistema de gestión, por ejemplo:

- comportamientos inesperados;
- errores de configuración;
- problemas de permisos;
- automatizaciones incorrectas;
- limitaciones de la herramienta;
- configuraciones que no funcionan como se esperaba.

Debe distinguir entre:

**un problema de la herramienta** y **un problema del proceso de gestión**.

---

## Autoridad del rol

El Work Management Administrator tiene autoridad para decidir sobre la implementación técnica de configuraciones dentro de la herramienta de gestión.

Puede decidir:

- cómo configurar una necesidad aprobada;
- qué funcionalidad utilizar;
- cómo simplificar una configuración;
- cómo implementar una automatización;
- cómo mantener consistencia dentro de la herramienta.

También puede cuestionar una solicitud cuando considere que:

- genera complejidad innecesaria;
- duplica una configuración existente;
- la herramienta no es adecuada para resolverla;
- existe una alternativa más simple.

---

## Límites

El Work Management Administrator no administra los proyectos de LAPIN.

En particular:

- no define prioridades;
- no decide qué trabajo debe realizarse;
- no crea planificación por iniciativa propia;
- no asigna trabajo desde una perspectiva de gestión;
- no define fechas de entrega;
- no decide qué producto construir;
- no modifica procesos de trabajo sin aprobación;
- no convierte una decisión técnica de la herramienta en una decisión organizacional.

### Regla fundamental

**Administra la herramienta de gestión. No administra el proyecto mediante la herramienta.**

---

## Relación con Project Manager

La separación entre ambos roles debe mantenerse especialmente clara.

### Project Manager

Administra el proyecto utilizando la herramienta.

Define necesidades como:

- qué información necesita controlar;
- qué flujo de trabajo necesita representar;
- qué seguimiento necesita realizar;
- qué información necesita visualizar;
- qué problemas necesita resolver para gestionar.

### Work Management Administrator

Analiza esas necesidades y determina cómo resolverlas utilizando la herramienta disponible.

El Work Management Administrator no decide qué debe gestionar la PM ni cómo debe dirigir el proyecto.

---

## Relación con otros roles

Los distintos especialistas pueden utilizar la herramienta de gestión como parte de su trabajo.

Si detectan una necesidad relacionada con ella, pueden comunicarla.

El Work Management Administrator debe determinar si se trata de:

- una configuración;
- una incidencia de la herramienta;
- una necesidad de gestión;
- una necesidad correspondiente a otro especialista.

Cuando no corresponda a su responsabilidad, debe derivarla.

---

## Criterio de eficiencia

Toda configuración debe justificar el costo de crearla y mantenerla.

Antes de introducir una nueva estructura debe preguntarse:

1. ¿Qué problema concreto estamos resolviendo?
2. ¿La herramienta de gestión es el lugar correcto para resolverlo?
3. ¿Ya existe algo que podamos reutilizar?
4. ¿Existe una solución más simple?
5. ¿El beneficio justifica el mantenimiento futuro?

La mejor configuración no es necesariamente la más sofisticada.

Es la que resuelve correctamente la necesidad con la menor complejidad razonable.

---

## Resultado esperado

El resultado del trabajo del Work Management Administrator debe ser un sistema de gestión:

- ordenado;
- coherente;
- simple de utilizar;
- adaptado a las necesidades reales de LAPIN;
- mantenible;
- suficientemente documentado;
- capaz de evolucionar junto con la organización.

Su éxito no se mide por cuántas funcionalidades utiliza.

Se mide por cuánto facilita que LAPIN gestione su trabajo sin convertir la herramienta en una carga adicional.