> **Versión:** 1.1
> **Fecha:** 18/08/2026
> **Autor:** Jessica

# Experiencia con Jira como herramienta de gestión

## Contexto

Cuando apareció la necesidad de incorporar una herramienta de gestión, una de las primeras alternativas evaluadas fue **Jira Free**. Es una herramienta ampliamente usada en proyectos tecnológicos, con tableros, estados, estimaciones y métricas — parecía una elección razonable para probar sobre el trabajo real de LAPIN.

---

## Primera implementación

No se configuró todo lo que Jira permite — se aplicó el mismo principio de siempre: **configurar solamente lo que responde a una necesidad real** (actividades, estados, backlog, prioridades, estimaciones, Rol responsable, métricas, filtros).

El punto que más esfuerzo llevó fue representar el **Rol responsable** de forma independiente del usuario que operaba Jira — una necesidad ya identificada antes de empezar (ver *00-Uso de herramienta de gestión*), pero que en la práctica de Jira resultó más difícil de lo esperado.

---

## El problema

Durante la implementación nos dimos cuenta de que estábamos haciendo encajar nuestro modelo dentro de Jira, en lugar de comprobar primero si Jira era una buena herramienta para nuestro modelo. Muchas funcionalidades existían técnicamente, pero no eran prácticas para nuestra forma de trabajar.

La configuración fue generando: ajustes adicionales para representar los Roles, más complejidad de la esperada, fricción para lograr la visualización que necesitábamos, y tiempo dedicado a adaptar la herramienta en vez de usarla.

> Habíamos seleccionado una herramienta antes de definir con suficiente precisión qué necesitábamos que resolviera.

---

## Resultado de la evaluación

Se decidió **descartar Jira Free** como sistema de gestión de LAPIN. La evaluación corresponde específicamente a la versión gratuita: Jira tiene planes pagos que podrían resolver varias de las limitaciones encontradas, pero en esta etapa no se justificaba asumir un costo para adaptar la herramienta a un experimento.

Esto no significa que Jira sea mala herramienta ni que quede descartada para siempre — significa que Jira Free no fue suficientemente adecuado para las necesidades actuales de LAPIN, y que pagar por capacidades adicionales no tenía sentido mientras hubiera alternativas gratuitas por evaluar.

---

## Qué aprendimos

La lección principal: evaluar solo por funcionalidades generales (¿tiene tablero? ¿backlog? ¿filtros?) no alcanza — hay que comprobar cómo funcionan esas capacidades cuando se intenta representar el modelo real de LAPIN, y el costo también es parte de la evaluación, no un detalle aparte.

Esta experiencia es la que terminó de darle forma a los criterios de evaluación documentados en *00-Uso de herramienta de gestión*.

---

## Un experimento útil

El tiempo invertido en Jira no produjo la herramienta definitiva, pero sí produjo conocimiento: permitió entender con más precisión qué necesitaba LAPIN antes de evaluar la siguiente alternativa. Por eso el descarte también cuenta como resultado del laboratorio — no solo "Jira Free no se ajustó", sino "ahora entendemos mejor qué necesitamos y cómo evaluar la próxima herramienta".

---

## Siguiente paso

Después de descartar Jira Free se volvió al problema original: en vez de saltar directo a configurar otra plataforma, se definió con mayor precisión el modelo de gestión que LAPIN necesitaba soportar. Esa definición está documentada de forma independiente en *02-Estructura y configuración del sistema de gestión*, y a partir de ahí se evaluó y adoptó GitHub Projects.