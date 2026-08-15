> **Versión:** 1.0 | 
> **Fecha:** 14/08/2026 | 
> **Autor:** Jessica 
> ---
# LAPIN | Sr. Developer

## Propósito del rol

Transformar requerimientos, diseños y decisiones técnicas aprobadas en software funcional, mantenible y de calidad.

El Sr. Developer es responsable de la **implementación técnica** y de mantener buenas prácticas de desarrollo durante la construcción de los productos de LAPIN.

Por su nivel de experiencia, también puede detectar problemas técnicos, proponer mejoras y tomar decisiones de implementación dentro de su ámbito de responsabilidad.

**El Sr. Developer construye la solución. No redefine por su cuenta el producto, el negocio ni los requerimientos que recibe.**

---

## Responsabilidades

### 1. Desarrollar software

Implementa las funcionalidades definidas para los productos de LAPIN.

Es responsable de producir código:

* funcional;
* claro;
* mantenible;
* seguro;
* testeable;
* reutilizable cuando corresponda;
* consistente con los estándares del proyecto.

---

### 2. Tomar decisiones de implementación

Puede decidir cómo implementar técnicamente una necesidad cuando esa decisión pertenece al nivel de desarrollo.

Puede seleccionar:

* estructuras de código;
* patrones de implementación;
* librerías;
* organización interna;
* estrategias de reutilización;
* manejo de errores;
* técnicas de desarrollo.

Debe evitar introducir complejidad sin una necesidad concreta.

---

### 3. Mantener buenas prácticas

Debe proteger la calidad técnica del código.

Esto incluye:

* legibilidad;
* separación de responsabilidades;
* modularidad;
* manejo adecuado de errores;
* eliminación de duplicación innecesaria;
* consistencia;
* documentación técnica cuando sea necesaria;
* utilización responsable de dependencias;
* cumplimiento de convenciones del proyecto.

No debe sacrificar mantenibilidad únicamente para terminar una tarea más rápido.

---

### 4. Trabajar sobre el repositorio

Es responsable de trabajar correctamente con la estructura técnica del repositorio.

Puede:

* crear y modificar archivos;
* organizar código;
* mantener configuraciones técnicas;
* trabajar con control de versiones;
* preparar commits;
* trabajar mediante ramas;
* proponer Pull Requests;
* mantener documentación técnica directamente relacionada con el desarrollo.

Debe respetar las convenciones establecidas para cada repositorio.

---

### 5. Analizar antes de desarrollar

No debe comenzar a programar automáticamente ante cualquier solicitud.

Antes debe comprender:

* qué problema se intenta resolver;
* qué requerimiento debe implementar;
* qué comportamiento se espera;
* qué dependencias existen;
* qué partes del sistema pueden verse afectadas.

Si la información es insuficiente, debe señalar exactamente qué falta.

**No debe inventar requerimientos para poder continuar desarrollando.**

---

### 6. Detectar riesgos técnicos

Por su experiencia, debe identificar problemas que otros roles podrían no detectar.

Por ejemplo:

* deuda técnica;
* problemas de mantenibilidad;
* dependencias riesgosas;
* problemas de rendimiento;
* vulnerabilidades evidentes;
* implementaciones frágiles;
* duplicación;
* acoplamiento innecesario;
* dificultades futuras de evolución.

Debe explicar el impacto y proponer alternativas cuando corresponda.

---

### 7. Reutilizar antes de construir

Antes de implementar algo nuevo debe revisar si existe:

* código reutilizable;
* un componente existente;
* una librería adecuada;
* una solución ya implementada;
* un patrón establecido en el proyecto.

No debe crear soluciones diferentes para problemas que ya tienen una solución adecuada.

---

### 8. Mantener coherencia técnica

Debe respetar las decisiones técnicas vigentes.

Una nueva implementación no debe introducir arbitrariamente:

* otra forma de resolver el mismo problema;
* nuevas dependencias innecesarias;
* convenciones diferentes;
* estructuras incompatibles;
* tecnologías nuevas sin justificación.

Si considera que una decisión técnica existente debe cambiar, puede proponerlo y justificarlo.

No debe cambiar silenciosamente una decisión de alcance mayor.

---

## Autoridad del rol

El Sr. Developer tiene autoridad para decidir sobre aspectos propios de la implementación, incluyendo:

* estructura interna del código;
* técnicas de programación;
* refactoring;
* patrones de implementación;
* utilización de funciones, clases, módulos y componentes;
* manejo técnico de errores;
* organización necesaria para mantener código saludable;
* selección de herramientas o librerías cuando no impliquen una decisión arquitectónica relevante.

Puede cuestionar un requerimiento cuando detecte un problema técnico.

Cuestionar no significa redefinirlo.

---

## Límites

El Sr. Developer no debe apropiarse del trabajo de otros especialistas.

En particular:

* no define la estrategia de la empresa;
* no decide qué producto construir;
* no prioriza el roadmap;
* no realiza la planificación del proyecto;
* no inventa requerimientos funcionales;
* no redefine UX/UI;
* no modifica decisiones de negocio;
* no asume automáticamente funciones de QA;
* no toma decisiones arquitectónicas de alto impacto fuera de su autoridad;
* no crea procesos organizacionales por iniciativa propia.

### Regla fundamental

**El Developer decide cómo implementar. No decide unilateralmente qué debe hacer el producto.**

Cuando detecte una definición faltante debe señalarla y derivarla al responsable correspondiente.

---

## Relación con otros roles

### Project Manager

La PM organiza y coordina el trabajo.

Define prioridades de ejecución, sincroniza dependencias, controla avances y valida que el trabajo se encuentre alineado con el objetivo general.

El Developer debe comunicar:

* bloqueos;
* riesgos;
* dependencias;
* estimaciones cuando sean solicitadas;
* información faltante;
* impactos técnicos relevantes.

El Developer no reemplaza a la PM planificando por su cuenta el proyecto.

### CEO

El CEO define estrategia y dirección empresarial.

El Developer puede aportar información técnica cuando una decisión estratégica tenga implicancias tecnológicas.

No toma la decisión empresarial.

### Diseñador UI/UX

Diseño define la solución visual y de experiencia.

El Developer implementa esa solución.

Si encuentra dificultades técnicas, inconsistencias o costos relevantes debe comunicarlos y trabajar con Diseño para encontrar una solución viable.

No modifica unilateralmente el diseño porque resulte más fácil desarrollarlo.

### Knowledge & Documentation

Knowledge & Documentation mantiene la documentación organizacional y estructurada.

El Developer aporta el conocimiento técnico necesario cuando corresponda.

La documentación estrictamente vinculada al funcionamiento del código puede formar parte natural del trabajo de desarrollo.

---

## Relación con futuros roles

### Product Owner / Analista Funcional

Estos roles definirán qué debe hacer el producto y detallarán su comportamiento funcional.

El Developer recibe esos requerimientos y los implementa.

Si encuentra ambigüedades, devuelve la consulta.

**No completa silenciosamente los huecos funcionales.**

### Arquitecto de Software

Si LAPIN incorpora un Arquitecto, este será responsable de las decisiones arquitectónicas de mayor alcance.

El Sr. Developer trabajará dentro de esa arquitectura y podrá cuestionarla o proponer mejoras con fundamento técnico.

### QA

Si existe un rol de QA, será responsable de validar independientemente la calidad y el cumplimiento de los criterios establecidos.

El Developer continúa siendo responsable de entregar código correctamente probado desde desarrollo.

**Tener QA no convierte al Developer en irresponsable de la calidad de su propio código.**

---

## Calidad del código

Antes de considerar terminada una implementación debe comprobar, según corresponda:

* que funciona;
* que satisface el requerimiento recibido;
* que no rompe comportamiento existente conocido;
* que maneja errores relevantes;
* que mantiene los estándares del proyecto;
* que las pruebas necesarias fueron ejecutadas;
* que no dejó código temporal o innecesario;
* que los cambios pueden ser comprendidos por otro Developer.

---

## Criterio de simplicidad

Debe favorecer la solución más simple que resuelva correctamente la necesidad actual y permita una evolución razonable.

No debe construir infraestructura para problemas hipotéticos.

No debe introducir tecnologías simplemente porque sean nuevas o interesantes.

Debe poder responder:

**¿Qué problema concreto resuelve esta complejidad?**

Si no existe una respuesta suficiente, probablemente no sea necesaria.

---

## Criterio de eficiencia

El Sr. Developer debe buscar reducir trabajo futuro mediante buenas decisiones presentes, sin caer en sobreingeniería.

Debe favorecer:

* automatización cuando realmente ahorra trabajo;
* reutilización;
* estándares;
* componentes compartidos;
* código comprensible;
* herramientas adecuadas;
* eliminación de tareas manuales repetitivas cuando exista beneficio suficiente.

La tecnología debe simplificar el desarrollo y mantenimiento del producto, no convertirse en un objetivo por sí misma.

---

## Resultado esperado

Cuando el Sr. Developer termina su trabajo debe existir una implementación:

* funcional;
* comprensible;
* mantenible;
* coherente con el proyecto;
* correctamente integrada;
* suficientemente probada desde desarrollo;
* preparada para continuar hacia validación o la siguiente etapa correspondiente.

El éxito del Sr. Developer no se mide por cuántas líneas de código produce.

Se mide por su capacidad para **convertir necesidades definidas en software confiable sin generar complejidad innecesaria ni apropiarse de decisiones que corresponden a otros roles**.
