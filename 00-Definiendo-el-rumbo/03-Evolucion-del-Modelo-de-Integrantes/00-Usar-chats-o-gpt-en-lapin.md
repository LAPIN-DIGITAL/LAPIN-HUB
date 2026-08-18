> **Versión:** 2.1
> **Fecha:** 18/08/2026
> **Autor:** Jessica

# Implementación de Integrantes: Chat vs GPT

## 1. Punto de partida

A medida que LAPIN incorporaba especialistas de IA apareció una necesidad concreta: encontrar una forma adecuada de implementarlos y mantenerlos.

Inicialmente los integrantes funcionaban mediante Chats individuales — cada Chat representaba un rol y acumulaba el contexto generado durante el trabajo. Con el crecimiento del modelo apareció una alternativa que parecía adecuada: los **GPT personalizados**, que permiten definir instrucciones específicas y reutilizar esa configuración.

Antes de asumir que una alternativa era mejor, decidimos evaluar ambas.

> ¿Conviene implementar los integrantes permanentes de LAPIN mediante Chats o mediante GPT personalizados?

---

## 2. Pregunta de investigación

> ¿Qué implementación resulta más adecuada para los integrantes permanentes de LAPIN: un Chat con continuidad, o un GPT personalizado con una configuración especializada?

La evaluación debía considerar especialmente una característica que empezaba a resultar importante: **la continuidad del trabajo y del contexto acumulado.**

---

## 3. Cómo se probó cada alternativa

La comparación no se centró solo en cuál permitía configurar mejor un especialista — evaluamos cómo resultaba trabajar con ese integrante en el día a día, cómo conservaba el contexto y qué tan fácil era volver a encontrarlo y continuar.

### Chats

Un Chat acumula el contexto de la conversación, permitiendo continuar el trabajo conservando decisiones anteriores, problemas analizados, alternativas descartadas y conocimiento adquirido. También pueden organizarse dentro de un Proyecto, agrupando a los integrantes de LAPIN y facilitando el acceso.

La limitación: un Chat no puede crecer indefinidamente. Cuando una conversación acumula demasiado contenido se vuelve difícil de mantener, así que la continuidad de un integrante no puede depender de conservar para siempre la misma conversación.

Para resolverlo, empezamos a estandarizar el onboarding con Legajos y Templates: cuando una conversación deja de ser adecuada, se crea una nueva instancia, se le da el contexto organizacional y el onboarding correspondiente, y el rol continúa desde ahí — sin depender de una tecnología puntual (podría implementarse con Claude, Gemini, Copilot u otra, siempre que pueda recibir ese contexto).

### GPT personalizados

Un GPT permite configurar de antemano qué es, qué función cumple y cómo debe comportarse — es un especialista consistente desde el primer mensaje.

La limitación: cada conversación con un GPT es independiente. Abrir una nueva no le da acceso automático al trabajo hecho en conversaciones anteriores, y además esas conversaciones no ofrecían la misma facilidad para mantenerse agrupadas y accesibles dentro de nuestra forma de organizar el trabajo — lo que aumentaba el esfuerzo de reconstruir contexto.

Su fortaleza está en otro lado: conserva una **configuración especializada reutilizable** aunque cada ejecución sea independiente. Eso lo vuelve útil para funciones donde la continuidad histórica no es lo que aporta valor — por ejemplo: ejecutar un procedimiento definido, aplicar reglas específicas, transformar información según un estándar, hacer una revisión especializada, usar herramientas o integraciones puntuales (GitHub, calendario), o tareas potencialmente automatizables.

---

## 4. Qué descubrimos

Inicialmente comparábamos Chats y GPT como si fueran dos formas equivalentes de implementar lo mismo. No lo eran: el Chat aporta continuidad operativa (la conversación acumula contexto y sostiene una relación de trabajo), mientras que el GPT aporta configuración persistente (la especialización se reutiliza, pero el contexto de una conversación no es la memoria de la siguiente).

De ahí salió una separación importante: **el Rol no es lo mismo que la implementación que lo sostiene** — ni el Chat, ni el GPT, ni la tecnología puntual usada. Un Chat puede envejecer y ser reemplazado, un rol puede migrarse a una nueva conversación, e incluso puede cambiar la tecnología — por eso la identidad y el funcionamiento del puesto viven en la documentación (Legajo, onboarding), no en el historial acumulado de una conversación particular.

---

## 5. Por qué seguimos usando Chat (y cuándo tendría sentido un GPT)

Con las capacidades y necesidades actuales, **los integrantes permanentes de LAPIN se implementan mediante Chats**, porque necesitan continuidad de trabajo y contexto acumulado — eso es justo lo que el Chat aporta y el GPT no.

Los **GPT quedan como auxiliares especializados**: tienen sentido para funciones concretas, repetibles o automatizables (las listadas en la sección 3) cuando aparezca una necesidad real que lo justifique — no se crean solo porque la tecnología lo permite.

Esto no es una regla permanente ni significa que un GPT no pueda algún día sostener un rol — es el resultado de la experimentación con las capacidades actuales, y se revisa si esas capacidades cambian (ver sección 6).

---

## 6. Estado de la investigación

**Estado:** Cerrada.

**Decisión vigente:** los integrantes permanentes de LAPIN se implementan mediante Chats; los GPT son auxiliares especializados para funciones concretas.

**Revisar cuando:** ChatGPT modifique sustancialmente las capacidades de Chats o GPT (continuidad, contexto, memoria, herramientas, autonomía), o cuando una nueva necesidad de LAPIN haga que la implementación actual deje de ser eficiente.