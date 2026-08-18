> **Versión:** 2.0 |  
> **Fecha:** 18/08/2026 |  
> **Autor:** Jessica  
> ---

# Implementación de Integrantes: Chat vs GPT

## 1. Punto de partida

A medida que LAPIN comenzó a incorporar distintos especialistas de Inteligencia Artificial apareció una necesidad concreta: encontrar una forma adecuada de implementar y mantener esos integrantes.

Inicialmente los integrantes funcionaban mediante Chats individuales. Cada Chat representaba un rol determinado y acumulaba el contexto generado durante el trabajo.

Con el crecimiento del modelo apareció una alternativa que parecía especialmente adecuada: utilizar **GPT personalizados**.

Un GPT permitía definir instrucciones específicas, configurar un especialista y reutilizar esa configuración. Esto generó una pregunta importante antes de continuar incorporando integrantes:

> **¿Conviene implementar los integrantes permanentes de LAPIN mediante Chats o mediante GPT personalizados?**

En lugar de asumir que una alternativa era mejor, decidimos evaluarlas antes de escalar el modelo.

---

## 2. Pregunta de investigación

> **¿Qué implementación resulta más adecuada para los integrantes permanentes de LAPIN: un Chat con continuidad o un GPT personalizado con una configuración especializada?**

La evaluación debía considerar especialmente una característica que comenzaba a resultar importante para nuestros integrantes: **la continuidad del trabajo y del contexto acumulado.**

---

## 3. Investigación / Experimentación

Evaluamos cómo se comportaban Chats y GPT personalizados cuando intentábamos utilizarlos como integrantes permanentes de LAPIN.

La comparación no se centró solamente en cuál herramienta permitía configurar mejor un especialista. Evaluamos cómo resultaba trabajar con ese integrante en el día a día, cómo conservaba el contexto y qué tan sencillo era volver a encontrarlo y continuar trabajando.

### Chats

Los Chats comenzaron siendo la forma natural de implementar nuestros integrantes. Un Chat representa un rol determinado y la conversación va acumulando el contexto generado durante el trabajo.

Esto permite continuar trabajando con el mismo integrante conservando decisiones anteriores, problemas analizados, alternativas descartadas, explicaciones y conocimiento adquirido durante la conversación.

También encontramos una ventaja operativa importante: los Chats pueden mantenerse organizados dentro de un Proyecto, permitiendo agrupar los integrantes relacionados con LAPIN y acceder fácilmente a ellos.

Sin embargo, la experimentación también mostró una limitación.

Un Chat no puede crecer indefinidamente.

Cuando una conversación acumula demasiado contenido puede volverse difícil de mantener y utilizar. Por lo tanto, la continuidad de un integrante no significa necesariamente conservar para siempre la misma conversación.

Esto nos llevó a separar nuevamente dos conceptos:

> **El integrante puede continuar aunque la instancia que lo implementa sea reemplazada.**

Para resolverlo comenzamos a estandarizar el onboarding mediante Legajos y Templates. Cuando una conversación deja de resultar adecuada, puede crearse una nueva instancia, proporcionarle el contexto organizacional y el onboarding correspondiente y continuar el rol desde allí.

Este mecanismo también evita depender completamente de ChatGPT.

El mismo rol podría posteriormente implementarse utilizando otra tecnología —por ejemplo Claude, Gemini, Copilot u otra alternativa— siempre que pueda recibir el contexto y las instrucciones necesarias para desempeñarlo.

### GPT personalizados

Los GPT personalizados ofrecían otra ventaja: permiten configurar previamente qué son, qué función cumplen, qué instrucciones deben seguir y cómo deben comportarse.

Esto los convierte en especialistas consistentes desde el momento en que comienza una conversación.

Sin embargo, encontramos limitaciones importantes para utilizarlos como integrantes permanentes dentro de nuestra forma actual de trabajo.

Las conversaciones iniciadas con un GPT son independientes. Abrir una nueva conversación permite volver a utilizar la configuración del especialista, pero no significa que esa nueva conversación conozca automáticamente el trabajo realizado en conversaciones anteriores.

También encontramos una dificultad organizativa: las conversaciones generadas con estos especialistas no ofrecían la misma facilidad para mantener agrupado y accesible el trabajo continuo del equipo dentro de nuestra organización actual.

Esto aumentaba el esfuerzo necesario para localizar conversaciones y reconstruir contexto.

La principal fortaleza del GPT estaba entonces en otro lugar.

El GPT puede conservar una **configuración especializada reutilizable** aunque cada ejecución o conversación sea independiente.

Esto resulta especialmente interesante para funciones donde la continuidad histórica no constituye el principal valor, por ejemplo:

- ejecutar un procedimiento definido;
- aplicar reglas específicas;
- transformar información siguiendo un estándar;
- realizar una revisión especializada;
- utilizar determinadas herramientas;
- conectarse con sistemas externos;
- ejecutar funciones relacionadas con GitHub;
- utilizar calendario u otras integraciones;
- realizar tareas potencialmente automatizables.

En estos casos no necesitamos necesariamente un integrante que recuerde toda su historia.

Necesitamos un especialista que **sepa qué es, qué debe hacer y cómo debe hacerlo cada vez que lo utilizamos**.

---

## 4. Qué descubrimos

La experimentación mostró que inicialmente estábamos comparando Chats y GPT como si fueran dos formas equivalentes de implementar lo mismo.

No lo eran.

El **Chat** aporta principalmente continuidad operativa. La conversación acumula contexto y permite desarrollar una relación de trabajo sostenida con el integrante.

El **GPT** aporta principalmente configuración persistente. Su especialización puede reutilizarse en nuevas conversaciones, pero el contexto generado durante una conversación no constituye necesariamente la memoria de la siguiente.

También descubrimos que ninguna implementación debe confundirse con el integrante.

Un Chat puede envejecer y ser reemplazado.

Un rol puede migrarse a una nueva conversación.

Incluso puede cambiar la tecnología utilizada para implementarlo.

Por eso comenzamos a utilizar documentación, templates y onboarding para que la identidad y funcionamiento del puesto no dependan exclusivamente del contexto acumulado dentro de una conversación.

Esto produjo tres separaciones importantes:

> **Rol ≠ Chat.**

> **Rol ≠ GPT.**

> **Integrante ≠ tecnología que actualmente lo implementa.**

La tecnología es el medio utilizado para desempeñar el puesto.

Con las capacidades actuales, encontramos dos usos diferentes:

> **Chat → integrante permanente que necesita continuidad y contexto de trabajo.**

> **GPT → especialista configurable y reutilizable para una función concreta.**

---

## 5. Conclusión

En el estado actual de las herramientas y del modelo de LAPIN, los **Chats resultan más adecuados para implementar integrantes permanentes que necesitan continuidad de trabajo y contexto acumulado**.

Los **GPT personalizados resultan más adecuados como especialistas auxiliares para funciones concretas, repetibles o potencialmente automatizables**.

Esto no significa que un GPT no pueda desempeñar un rol ni que esta separación deba mantenerse permanentemente.

Representa el resultado de la experimentación realizada con las capacidades y necesidades actuales.

---

## 6. Decisión adoptada

LAPIN adopta actualmente el siguiente criterio:

> **Chats = integrantes estables.**  
> **GPT = auxiliares especializados.**

Los roles permanentes continuarán implementándose inicialmente mediante Chats.

Las funciones especializadas podrán convertirse en GPT cuando aparezca una necesidad concreta que justifique hacerlo.

No se crearán GPT simplemente porque la tecnología lo permita.

La incorporación debe resolver un problema o aportar una mejora suficiente para justificarla.

---

## 7. Estado de la investigación

**Estado:** Cerrada.

**Decisión vigente:** Los integrantes permanentes de LAPIN se implementan actualmente mediante Chats. Los GPT se consideran principalmente auxiliares especializados para funciones concretas.

**Revisar cuando:** ChatGPT modifique sustancialmente las capacidades de Chats o GPT, especialmente en aspectos relacionados con continuidad, contexto, memoria, herramientas o autonomía, o cuando una nueva necesidad de LAPIN haga que la implementación actual deje de resultar eficiente.