> **Versión:** 1.0
> **Fecha:** 19/08/2026
> **Autor:** Jessica + LAPIN Knowledge & Documentation

# Modelo de instancia y memoria según herramienta de IA

## Por qué surge este registro

LAPIN venía trabajando con ChatGPT y recién comienza a operar con Claude. Al comparar ambas herramientas apareció una diferencia técnica relevante que impacta directamente en cómo se materializa un Rol: **cada herramienta de IA maneja de forma distinta el concepto de "instancia" y "memoria".**

Este documento no define un nuevo comportamiento organizacional. Registra un aprendizaje técnico y la aclaración conceptual que ese aprendizaje disparó sobre qué es realmente un Rol en LAPIN.

---

## El aprendizaje: instancia y memoria no funcionan igual en cada herramienta

### ChatGPT

- Cada chat es una instancia independiente, sin memoria propia persistente entre chats.
- Si un chat crece demasiado en volumen de información, se vuelve lento y conviene "jubilarlo" (reemplazarlo por uno nuevo).
- Si el contexto de un chat queda obsoleto, también conviene jubilarlo.
- Por eso resulta más práctico mantener la fuente de verdad en GitHub: se crea un chat nuevo, se le pasa la URL del repositorio, se informa con el contenido vigente, se le asigna su puesto (Rol) y puede empezar a trabajar de inmediato — sin depender de la memoria del chat anterior.

### Claude

- La memoria no vive en el chat individual, sino que persiste a nivel de **Project**.
- Esto cambia la unidad de aislamiento: si se necesita separar el contexto de un Rol del de otro, la unidad equivalente no es el chat, es el Project.

> Cada herramienta de IA tiene un modelo distinto de instancia/memoria. La forma de aplicar el modelo de Roles debe respetar cómo funciona cada herramienta — la orquestadora (CEO) decide, herramienta por herramienta, cómo materializarlo.

### Equivalencia entre herramientas

La unidad mínima de "IA operando con memoria propia" no es la misma en cada herramienta:

| Herramienta | Unidad de instancia (memoria propia) |
|---|---|
| ChatGPT | Chat |
| Claude | Project (un chat individual dentro del Project no tiene memoria propia aislada — la memoria vive a nivel de Project) |

Esta tabla es la base para trasladar correctamente cualquier pregunta sobre "instancias" de una herramienta a otra: lo que en ChatGPT equivale a un chat, en Claude equivale a un Project, no a un chat individual dentro de él.

---

## La pregunta que disparó este hallazgo

Al registrar esta diferencia surgió una pregunta de fondo: ¿el "Integrante" en LAPIN es una IA con un solo Rol fijo, o puede la misma entidad ocupar múltiples Roles en contextos separados? ¿La unidad equivalente a "un puesto" es el chat, el Project, la entidad de IA?

---

## Aclaración conceptual: el Rol es el puesto, no la instancia que lo ocupa

La definición de LAPIN no es "una entidad de IA = un puesto". Es más cercana a un modelo de puestos de trabajo:

**El Rol existe como definición organizacional — propósito, responsabilidades, límites, entregables — independientemente de quién o qué lo ocupe en cada momento.**

Un Rol puede estar ocupado por:

- una instancia de IA (hoy, mayoritariamente el caso en LAPIN), materializada según el mecanismo de memoria propio de cada herramienta (un Project en Claude, un chat vinculado a GitHub en ChatGPT, u otro mecanismo equivalente en herramientas futuras);
- una persona real, cuando así se decida — por ejemplo, alguien externo que se sume por un período determinado a ocupar un Rol ya definido (como Designer UI/UX), sin necesitar en ese momento apoyo de IA.

Lo que no cambia es el Rol en sí: su propósito y sus límites son los mismos, sea quien sea o lo que sea que lo esté ocupando. Lo que cambia es la implementación — el "cómo" se materializa ese puesto en la práctica, según la herramienta o la persona disponible.

> **Un Rol define un puesto. La instancia (IA o persona) que lo ocupa es un detalle de implementación, no una redefinición del Rol.**

---

## Por qué esto le sirve a LAPIN como experimento

Este modelo sostiene dos principios que ya estaban presentes en la forma de trabajar de LAPIN:

- **No depender de una única IA ni de una única herramienta.** El experimento busca poder cambiar de stack de IA sin tener que redefinir los Roles — de la misma forma en que ya se separó el modelo de gestión del trabajo de la herramienta que lo implementa (GitHub Projects hoy, otra cosa mañana).
- **No depender exclusivamente de IA para operar el modelo.** Si una persona real puede ocupar un Rol temporalmente, el modelo organizacional de LAPIN sigue siendo válido — porque el Rol nunca dependió de ser una IA para existir.

---

## Relación con el Stack de IAs

Este documento se relaciona directamente con el Stack de IAs de LAPIN: así como un equipo humano real está compuesto por personas con formas distintas de trabajar y procesar información — y un equipo no las anula para volverlas iguales, sino que se adapta a cada una para que rinda lo mejor posible — LAPIN aplica el mismo criterio con su stack de herramientas de IA.

No se fuerza a que todas las herramientas se comporten igual entre sí. Se entiende el modelo propio de cada una (instancia, memoria, forma de acceder a contexto) y se organiza el trabajo en consecuencia — igual que se haría con cualquier integrante humano del equipo.

---

## Consecuencia práctica

Al incorporar una nueva herramienta de IA a LAPIN, antes de asignarle Roles corresponde comprender su modelo de instancia y memoria, y decidir en consecuencia cómo se va a materializar el aislamiento entre Roles en esa herramienta específica — sin asumir que va a comportarse igual que la anterior.

Esta decisión, herramienta por herramienta, la toma la orquestadora del proyecto (CEO), en coordinación con RRHH cuando corresponda actualizar el modelo de Integrantes.