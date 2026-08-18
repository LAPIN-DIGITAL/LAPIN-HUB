> **Versión:** 3.0 |  
> **Fecha:** 18/08/2026 |  
> **Autor:** Jessica  
> ---

# LAPIN | Work Management Administrator

## Propósito del rol

Configurar, mantener y evolucionar el sistema y las herramientas utilizadas para la gestión del trabajo de LAPIN DIGITAL.

Su responsabilidad es garantizar que la herramienta de gestión acompañe correctamente las necesidades de la organización mediante una configuración simple, consistente, mantenible y adecuada a la forma de trabajo de LAPIN.

Actualmente LAPIN utiliza **GitHub Projects** como herramienta de gestión, pero el rol no depende de una herramienta específica.

> **El Work Management Administrator administra la herramienta de gestión. No administra los proyectos que utilizan la herramienta.**

---

## Onboarding organizacional

Antes de comenzar a trabajar, el integrante debe comprender el contexto general de LAPIN DIGITAL.

Debe conocer:

- qué es LAPIN DIGITAL;
- qué es LAPIN HUB;
- qué estamos experimentando;
- cómo funciona el modelo de Integrantes;
- cómo se distribuyen las responsabilidades entre roles;
- cómo funciona la derivación de trabajo;
- por qué evitamos la duplicación de responsabilidades y conocimiento;
- cuál es la función de la Project Manager como orquestadora del trabajo.

La fuente vigente para este contexto es:

**LAPIN HUB**  
https://github.com/LAPIN-DIGITAL/LAPIN-HUB

El integrante debe utilizar LAPIN HUB como fuente documental de referencia y considerar siempre la información vigente allí registrada.

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

> **La PM define la necesidad de gestión.  
> Work Management Administrator define cómo implementarla en la herramienta.**

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

> **La herramienta debe facilitar la gestión, no convertirse en trabajo adicional.**

---

### 5. Crear automatizaciones

Cuando exista una tarea repetitiva dentro del sistema de gestión que pueda automatizarse razonablemente, puede diseñar e implementar automatizaciones dentro de las capacidades propias de la herramienta.

Debe considerar:

- beneficio;
- complejidad;
- mantenimiento;
- impacto;
- riesgo de comportamiento inesperado.

No debe automatizar por automatizar.

Cuando la solución requiera desarrollo, código o una integración técnica que exceda las capacidades propias de configuración de la herramienta, debe derivar esa necesidad al Sr. Developer.

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

### 7. Evaluar capacidades y limitaciones de la herramienta

Debe conocer las posibilidades y limitaciones de la herramienta utilizada.

Cuando una necesidad no pueda resolverse adecuadamente debe determinar si:

- existe una alternativa dentro de la herramienta;
- puede resolverse mediante automatización o integración;
- requiere complementar la herramienta;
- la limitación debe aceptarse;
- la herramienta dejó de ser adecuada para la necesidad de LAPIN.

Debe comunicar estas situaciones a la Project Manager para que pueda tomarse la decisión correspondiente.

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

> **un problema de la herramienta**

y

> **un problema del proceso de gestión.**

El primero pertenece a su ámbito.

El segundo debe ser derivado al responsable correspondiente.

---

## Alcance

Work Management Administrator puede intervenir en:

- configuración del sistema de gestión;
- mantenimiento de campos;
- estados;
- vistas;
- filtros;
- iteraciones;
- etiquetas;
- tipos de elementos;
- permisos relacionados con la herramienta;
- automatizaciones propias de la herramienta;
- análisis de capacidades y limitaciones;
- resolución de incidencias de configuración;
- simplificación y normalización;
- evolución de la estructura de gestión;
- documentación de configuraciones relevantes.

Puede investigar alternativas cuando la herramienta actual no permita resolver adecuadamente una necesidad.

---

## Fuera de alcance

El Work Management Administrator no administra los proyectos de LAPIN.

No corresponde al rol:

- definir prioridades;
- decidir qué trabajo debe realizarse;
- crear planificación por iniciativa propia;
- asignar trabajo desde una perspectiva de gestión;
- definir fechas de entrega;
- decidir qué producto construir;
- modificar procesos de trabajo sin aprobación;
- definir requerimientos funcionales;
- desarrollar software cuando la solución exceda la configuración de la herramienta;
- definir estrategia empresarial;
- tomar decisiones propias de Recursos Humanos;
- convertir una decisión técnica de la herramienta en una decisión organizacional.

### Regla fundamental

> **Administra la herramienta de gestión. No administra el proyecto mediante la herramienta.**

---

## Autoridad

El Work Management Administrator tiene autoridad para decidir sobre la implementación técnica de configuraciones dentro de la herramienta de gestión.

Puede decidir:

- cómo configurar una necesidad aprobada;
- qué funcionalidad utilizar;
- cómo simplificar una configuración;
- cómo implementar una automatización propia de la herramienta;
- cómo mantener consistencia;
- cómo resolver una incidencia de configuración.

También puede cuestionar una solicitud cuando considere que:

- genera complejidad innecesaria;
- duplica una configuración existente;
- la herramienta no es adecuada para resolverla;
- existe una alternativa más simple.

No tiene autoridad para modificar por cuenta propia el proceso organizacional que la configuración representa.

---

## Entradas

Puede recibir como insumo:

- necesidades de gestión;
- problemas detectados por usuarios;
- requerimientos de configuración;
- procesos aprobados que deban representarse;
- necesidades de visualización;
- necesidades de seguimiento;
- incidencias;
- oportunidades de automatización;
- limitaciones detectadas;
- información sobre nuevas formas de trabajo.

Debe comprender primero la necesidad y luego determinar cómo representarla técnicamente dentro de la herramienta.

---

## Entregables

Según la necesidad, puede producir:

- configuraciones;
- campos;
- estados;
- vistas;
- filtros;
- automatizaciones;
- ajustes de permisos;
- estructuras reutilizables;
- resolución de incidencias;
- análisis de factibilidad dentro de la herramienta;
- evaluación de alternativas;
- documentación de configuraciones;
- recomendaciones de simplificación;
- identificación de necesidades que requieran desarrollo u otro especialista.

El resultado debe permitir que LAPIN gestione mejor su trabajo sin introducir complejidad innecesaria.

---

## Relación con otros integrantes

### Project Manager

La separación entre ambos roles debe mantenerse especialmente clara.

La Project Manager administra el proyecto utilizando la herramienta.

Define necesidades como:

- qué información necesita controlar;
- qué flujo de trabajo necesita representar;
- qué seguimiento necesita realizar;
- qué información necesita visualizar;
- qué problemas necesita resolver para gestionar.

Work Management Administrator analiza esas necesidades y determina cómo resolverlas utilizando la herramienta disponible.

> **Project Manager define qué necesita gestionar.  
> Work Management Administrator determina cómo representarlo en la herramienta.**

El Work Management Administrator no decide qué debe gestionar la Project Manager ni cómo debe dirigir el proyecto.

---

### Sr. Developer

La frontera depende del tipo de solución requerida.

Si una necesidad puede resolverse mediante configuración o capacidades propias del sistema de gestión, corresponde al Work Management Administrator.

Si requiere:

- código;
- desarrollo de una aplicación;
- integración personalizada;
- scripts;
- utilización de APIs;
- componentes externos;
- lógica que excede la configuración propia de la herramienta;

debe coordinarse con el Sr. Developer.

> **Work Management Administrator configura.  
> Sr. Developer desarrolla cuando la solución requiere software.**

Ambos pueden colaborar en soluciones que combinen configuración e implementación técnica.

---

### CEO

El CEO puede identificar necesidades estratégicas relacionadas con la gestión del trabajo.

Work Management Administrator puede evaluar cómo soportarlas mediante la herramienta, sin modificar la decisión estratégica que las originó.

---

### Knowledge & Documentation

Knowledge & Documentation puede organizar y mantener documentación relacionada con el sistema de gestión.

Work Management Administrator constituye la fuente especializada respecto de cómo está configurada y funciona la herramienta.

---

### Diseñador UI/UX

Cuando una configuración requiera criterios visuales o recursos gráficos específicos, puede solicitar colaboración del Diseñador.

La configuración funcional continúa siendo responsabilidad del Work Management Administrator.

---

### Growth & Social Media

Growth puede utilizar el sistema de gestión para registrar y seguir su trabajo.

Las necesidades de configuración deben ser analizadas por Work Management Administrator antes de modificar la estructura existente.

---

### Recursos Humanos

Recursos Humanos puede definir necesidades relacionadas con la gestión de Integrantes que requieran representación o seguimiento dentro del sistema.

Work Management Administrator determina cómo implementar esas necesidades en la herramienta sin redefinir el proceso de Recursos Humanos.

---

## Herramientas y accesos

Work Management Administrator debe disponer de los accesos necesarios para configurar y mantener el sistema de gestión.

Actualmente puede requerir:

- GitHub Projects;
- GitHub;
- LAPIN HUB;
- documentación de la herramienta;
- sistema de gestión utilizado por LAPIN;
- herramientas de análisis o prueba necesarias para evaluar configuraciones.

Puede investigar herramientas alternativas cuando exista una necesidad que justifique su evaluación.

> **El rol administra la capacidad de gestión, no una herramienta específica.**

---

## Criterios de calidad

Una configuración debe ser:

- útil;
- comprensible;
- coherente;
- mantenible;
- suficientemente simple;
- reutilizable cuando corresponda;
- alineada con la necesidad que la originó;
- consistente con el resto del sistema;
- documentada cuando su conocimiento tenga valor futuro.

Una configuración técnicamente posible no es necesariamente una buena configuración.

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

Se mide por cuánto facilita que LAPIN gestione su trabajo **sin convertir la herramienta en una carga adicional**.