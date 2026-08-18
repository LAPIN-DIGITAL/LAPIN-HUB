> **Versión:** 2.1
> **Fecha:** 18/08/2026
> **Autor:** Jessica

# Importancia de incorporar una herramienta de gestión

## Por qué apareció la necesidad

A medida que LAPIN empezó a trabajar con más Roles y actividades en paralelo, apareció un problema práctico.

LAPIN HUB conserva el conocimiento generado: qué hicimos, qué decidimos, por qué y qué aprendimos. Pero eso no alcanza para gestionar el trabajo cotidiano.

Después de algunos días necesitábamos poder responder rápido: ¿dónde habíamos quedado? ¿qué estábamos haciendo? ¿qué quedó pendiente? ¿qué Rol tiene trabajo por hacer? ¿qué está bloqueado? ¿qué es prioritario? ¿qué sigue después?

Depender de recordarlo funciona con poco trabajo, pero deja de ser sostenible a medida que crece. Por eso LAPIN necesita complementar su memoria documental con un **sistema de gestión del trabajo**.

> LAPIN HUB conserva el conocimiento y el camino recorrido. El sistema de gestión permite saber dónde estamos y cómo continuar.

---

## Qué esperamos del sistema

No buscamos solamente una lista de tareas. El sistema debe permitir entender rápidamente: qué trabajo existe, en qué estado está, qué Rol es responsable, qué prioridad tiene, a qué período pertenece, cuánto se estima y se completa, y qué resultados se producen.

También debe generar información que después permita analizar cómo funciona LAPIN como organización — forma parte de la infraestructura del laboratorio, no es solo una lista de pendientes.

---

## Una particularidad de LAPIN: Roles, no usuarios

LAPIN no trabaja con personas reales con cuenta de usuario — trabaja con **Roles**, que pueden estar ocupados por una IA o por una persona. Eso significa que quien opera la herramienta no necesariamente es quien responde por el trabajo.

Por eso, al evaluar una herramienta, necesitábamos comprobar especialmente que pudiera representar a nuestros Roles como información estructurada — no depender solo de los usuarios registrados en la plataforma. *(Cómo se implementó ese campo en detalle está documentado en 02-Estructura-y-configuración-del-sistema-de-gestión.)*

---

## Criterios para evaluar una herramienta

La experiencia nos enseñó que antes de invertir tiempo configurando una herramienta hay que comprobar si puede representar nuestro modelo de trabajo. Como mínimo, estas son las preguntas que aplicamos:

1. **¿Permite campos configurables para representar Roles**, independientes del usuario que opera la herramienta?
2. **¿Podemos diferenciar los Roles a simple vista**, sin abrir cada actividad individualmente?
3. **¿El tablero es amigable?** No alcanza con que una función exista si usarla implica demasiada navegación o carga administrativa.
4. **¿Podemos filtrar y agrupar usando campos configurables** como el Rol responsable?
5. **¿Permite tags o etiquetas** para clasificaciones flexibles que no justifiquen un campo estructurado propio?
6. **¿Puede integrarse o automatizarse con IA** a futuro, aunque no sea necesario desde el día uno?
7. **¿Puede relacionarse con un sistema de registro de horas**, aunque viva en otra herramienta, siempre que la relación entre ambos sea confiable?

### Otros aspectos considerados
Backlog, estados y flujo de trabajo, prioridades, estimación, métricas, trazabilidad por fechas, costo, facilidad de mantenimiento y posibilidad de crecimiento. Que una herramienta tenga muchas funciones no la vuelve automáticamente una buena opción — lo que importa es que lo que realmente necesitamos sea **práctico de usar**.

---

## Criterio adoptado

Primero definimos cómo necesita trabajar LAPIN. Después elegimos la herramienta que mejor se adapte a ese modelo — nunca al revés. La herramienta puede cambiar con el tiempo; lo que debe mantenerse es la capacidad de organizar el trabajo de LAPIN de forma clara, medible y con la menor fricción posible.

> La herramienta acompaña el proceso. No lo define.