> **Versión:** 1.0 |  
> **Fecha:** 16/08/2026 |  
> **Autor:** Jessica  
> ---

# Evolución del modelo de Integrantes de LAPIN DIGITAL

## Introducción

El modelo de Integrantes de LAPIN DIGITAL no fue diseñado completamente desde el comienzo. Fue apareciendo y evolucionando a medida que trabajábamos: probamos formas de organizarnos, incorporamos especialistas, descartamos herramientas, modificamos roles, encontramos problemas y fuimos ajustando el modelo.

Este documento registra ese recorrido. No busca explicar las reglas actuales de los integrantes —para eso existe el **Reglamento de los Integrantes**— ni registrar quién está activo o cuándo ingresó —para eso existe el **Histórico de Integrantes**—.

Busca responder otra pregunta:

> **¿Cómo llegamos al modelo actual y qué aprendimos durante el camino?**

LAPIN HUB es un laboratorio. Por eso consideramos importante documentar no solamente aquello que funcionó, sino también las pruebas, errores y decisiones que nos permitieron llegar hasta acá.

---

# 1. Dejamos de trabajar con una única IA

En un principio, utilizar Inteligencia Artificial significaba principalmente conversar con un asistente para resolver necesidades muy diferentes: programación, documentación, análisis, diseño, gestión, aspectos legales o comunicación.

Pero apareció un problema: cuanto más diferentes eran las necesidades, más difícil resultaba mantener especialización, contexto y responsabilidades claras.

Entonces surgió una pregunta:

> **¿Qué pasaría si en lugar de utilizar una IA que hace de todo construimos un equipo de especialistas?**

La idea comenzó a parecerse mucho más a una organización tradicional: un CEO, un Developer, un especialista en UI/UX, un Analista Funcional, un responsable de documentación, cada uno con una responsabilidad diferente.

A partir de ese momento comenzamos a dejar de pensar solamente en conversaciones con una IA. Empezamos a pensar en **integrantes de una organización**.

---

# 2. Nacen los primeros Lapines

Los primeros integrantes fueron creados asignando a distintas instancias de IA funciones específicas. Cada una comenzó a recibir un puesto y, con el tiempo, también empezamos a definir su propósito, responsabilidades, autoridad, alcance, límites y relación con otros especialistas.

Internamente comenzamos a llamar a estos integrantes **Lapines**.

La intención era que cada uno funcionara de manera similar a un especialista dentro de una empresa: no solamente debía ejecutar tareas, también debía comprender cuál era su responsabilidad dentro del conjunto.

---

# 3. Descubrimos la importancia de la especialización

Muy rápidamente apareció uno de los primeros aprendizajes: una Inteligencia Artificial puede tener capacidad para resolver una gran variedad de problemas, pero eso no significa que deba resolverlos todos.

Si el Developer empieza a tomar decisiones de producto, el diseñador define arquitectura y el CEO comienza a redactar documentación, volvemos al mismo problema que intentábamos resolver: todos pueden hacer de todo y nadie tiene una responsabilidad clara.

Por eso empezamos a establecer fronteras entre los puestos. La capacidad de hacer algo dejó de significar automáticamente tener autoridad para hacerlo. Cuando una necesidad pertenece a otra especialidad, debe derivarse.

Esto comenzó a reducir duplicación, superposición, pérdida de foco y decisiones tomadas por el especialista incorrecto. La especialización empezó a convertirse en uno de los principios centrales del modelo.

---

# 4. La coordinación también tiene un costo

Al principio podía parecer conveniente crear un especialista diferente para cada necesidad, pero apareció otro problema: cada integrante adicional también necesita ser gestionado.

Hay que proporcionarle contexto, explicarle necesidades, asignarle trabajo, responder consultas, revisar resultados, validar entregables y coordinarlo con otros integrantes.

Aunque el integrante sea una IA, **su incorporación no tiene costo cero**. Consume tiempo de coordinación.

Esto produjo otro aprendizaje:

> **Tener más especialistas no significa necesariamente ser más productivos.**

Un nuevo rol debe aportar suficiente valor como para justificar el costo adicional de incorporarlo y coordinarlo. Por eso dejamos de crear roles preventivamente: primero aparece una necesidad, después evaluamos si un integrante existente puede resolverla correctamente y solamente cuando realmente necesitamos una nueva especialidad incorporamos otro integrante.

---

# 5. Empezamos a construir el onboarding de cada puesto

A medida que aumentaba la cantidad de integrantes apareció otra necesidad. No alcanzaba con decir: *“Ahora sos el Developer”*. Era necesario explicar qué significaba ocupar ese puesto dentro de LAPIN.

Comenzamos entonces a desarrollar documentos específicos para cada rol. Estos documentos fueron evolucionando hasta convertirse en los **Legajos de Rol**.

El Legajo funciona como onboarding del integrante y define, entre otras cosas:

- quién es;
- qué función cumple;
- qué responsabilidades tiene;
- qué autoridad posee;
- qué está dentro y fuera de su alcance;
- cómo se relaciona con otros especialistas;
- qué resultado se espera de su trabajo.

Esto permitió comenzar a estandarizar la incorporación de nuevos Lapines.

---

# 6. Probamos Chats y GPT personalizados

Cuando los roles comenzaron a consolidarse apareció una pregunta tecnológica:

> **¿Cuál es la mejor manera de implementar un integrante de LAPIN dentro de ChatGPT?**

Evaluamos utilizar GPT personalizados para representar nuestros puestos permanentes. La idea parecía lógica: podíamos crear un GPT para cada especialidad, proporcionarle instrucciones y reutilizarlo.

Pero decidimos probarlo antes de trasladar toda la organización. La evaluación consumió tiempo y ese tiempo también formó parte del experimento.

Durante las pruebas observamos que nuestros integrantes permanentes necesitaban especialmente continuidad, contexto acumulado, facilidad para retomar conversaciones, organización y acceso rápido al historial de trabajo.

En el estado de las herramientas evaluadas, los Chats resultaron más prácticos para esa función. Los GPT, en cambio, podían resultar útiles como auxiliares especializados para tareas concretas.

La decisión actual quedó:

> **Chats = integrantes estables.**  
> **GPT = auxiliares especializados.**

Esta decisión no se considera definitiva. La tecnología puede evolucionar y LAPIN puede volver a evaluarla.

El aprendizaje más importante fue otro:

> **Antes de escalar una decisión tecnológica a toda la organización, conviene probarla.**

Invertir tiempo en validar una decisión puede evitar multiplicar posteriormente una solución incorrecta.

---

# 7. Descubrimos que el contexto puede ser un activo o un problema

La continuidad de una instancia permite acumular conocimiento sobre LAPIN, las decisiones tomadas, la forma de trabajo y los problemas anteriores. Ese conocimiento puede ser extremadamente valioso.

Pero también descubrimos que el contexto puede envejecer. Una instancia puede acumular tantas instrucciones, decisiones antiguas o cambios de dirección que ese conocimiento empiece a interferir con su nueva función.

Aparecieron entonces dos posibilidades:

- **Evolucionar un integrante:** cuando el conocimiento acumulado continúa siendo útil, el integrante puede evolucionar hacia un nuevo puesto.
- **Dar de baja y comenzar nuevamente:** cuando el contexto anterior genera interferencias o la nueva función requiere una perspectiva sustancialmente diferente, puede resultar más eficiente crear una nueva instancia.

Esto convirtió al contexto en algo que también debe gestionarse.

**No siempre más contexto significa mejor resultado.**

---

# 8. Primeros casos reales de evolución

El modelo comenzó a ponerse a prueba con integrantes reales.

### Asistente de Redacción

Inicialmente existía un puesto dedicado principalmente a mejorar y redactar documentación. Con el tiempo descubrimos que esa función era demasiado limitada: LAPIN no necesitaba solamente alguien que escribiera mejor, sino organizar, estructurar, mantener y convertir en reutilizable el conocimiento generado.

El puesto de Asistente de Redacción fue dado de baja y surgió **Knowledge & Documentation**, con un alcance más amplio y un contexto renovado.

### Jira Administrator

También ocurrió el caso contrario. Inicialmente incorporamos un especialista para administrar Jira. Posteriormente Jira fue descartado como herramienta de gestión, pero el conocimiento acumulado por el integrante continuaba siendo útil y la necesidad tampoco había desaparecido.

Seguíamos necesitando alguien responsable de administrar nuestro sistema de gestión. En este caso decidimos conservar al integrante y evolucionar su puesto hacia **Work Management Administrator**.

Esto permitió comprobar que:

> **Un integrante y el puesto que ocupa no son necesariamente la misma cosa.**

---

# 9. Las herramientas son reemplazables

El caso de Jira produjo otro aprendizaje. Habíamos definido inicialmente un puesto alrededor de una herramienta: **Jira Administrator**.

Cuando Jira dejó de utilizarse descubrimos que habíamos confundido la herramienta con la necesidad. La herramienta desapareció, pero la necesidad permaneció.

Esto nos llevó a definir puestos de manera más independiente de las tecnologías utilizadas. Hoy hablamos de **Work Management Administrator**.

La herramienta puede ser GitHub Projects hoy y otra diferente mañana. El puesto continúa teniendo sentido mientras exista la necesidad que justifica su función.

---

# 10. Creamos identidad para los roles

Cuando comenzaron a aumentar los integrantes apareció una necesidad operativa: necesitábamos identificarlos fácilmente dentro del sistema de gestión.

Un código correlativo como `ROL-006` podía ser técnicamente correcto, pero obligaba a recordar qué significaba cada número. Decidimos utilizar códigos reconocibles como `LD-CEO`, `LD-SRDEV`, `LD-UIUX`, `LD-WRITER` o `LD-WMAdm`.

El criterio fue simple:

> **El código debe permitir reconocer rápidamente la función.**

Esto también nos obligó a diferenciar conceptos que hasta entonces utilizábamos casi indistintamente:

- **Integrante:** quién forma parte de LAPIN.
- **Lapin:** denominación interna de un integrante.
- **Rol / Puesto:** función que desempeña.
- **Código:** identificador reconocible de esa función.
- **Tecnología:** herramienta mediante la cual ese integrante realiza su trabajo.

Esta separación permitió que el modelo comenzara a independizarse de una tecnología específica.

---

# 11. Dejamos de pensar exclusivamente en integrantes IA

Inicialmente los Lapines eran instancias de Inteligencia Artificial, pero al formalizar el modelo apareció una conclusión importante: la estructura organizacional no necesitaba depender de que el integrante fuera una IA.

Un Integrante de LAPIN puede ser una persona, una instancia de Inteligencia Artificial, un GPT, un agente especializado u otra implementación futura capaz de asumir un puesto.

Lo importante es que exista una función, responsabilidades, autoridad y límites definidos.

Esto permite que el modelo pueda combinar personas e Inteligencias Artificiales dentro de una misma organización.

---

# 12. Empezamos a registrar el trabajo

Durante las primeras etapas, gran parte del trabajo ocurría directamente dentro de las conversaciones: pedíamos algo, trabajábamos, llegábamos a un resultado y continuábamos con lo siguiente.

Funcionaba, pero teníamos un problema: podíamos observar lo que habíamos construido, pero no cuánto esfuerzo había requerido construirlo.

Para LAPIN HUB esto era especialmente importante. El objetivo del laboratorio no es solamente demostrar que algo puede hacerse; también queremos comprender **cuánto cuesta hacerlo**.

Por eso comenzamos a registrar las actividades en nuestro sistema de gestión. Antes de comenzar una nueva actividad registramos título, descripción y tipo de actividad. Durante el trabajo registramos decisiones, cambios, bloqueos o hallazgos importantes. Cuando terminamos registramos el resultado, los entregables y el tiempo utilizado.

Esto cambió nuestra capacidad para observar el experimento.

Ya no queremos decir solamente:

> "Construimos esto y funcionó."

Queremos poder decir:

> "Construimos esto, funcionó y necesitamos aproximadamente 50 horas para conseguirlo."

La diferencia es fundamental. Un resultado que funciona pero necesita cinco años de trabajo puede no representar un modelo eficiente.

---

# 13. Empezamos a medir si el modelo realmente funciona

Registrar actividades también permitió formular una pregunta todavía más importante:

> **¿Nuestro modelo organizacional realmente funciona?**

No alcanza con crear diferentes instancias de IA, asignarles nombres de puestos y conseguir resultados. Queremos comprobar si cada integrante puede desempeñarse como un especialista dentro de una organización.

Necesitamos evaluar dos dimensiones:

**Eficacia:** ¿el integrante consigue correctamente el resultado esperado para su puesto?

**Eficiencia:** ¿cuánto tiempo, esfuerzo, corrección y coordinación necesitamos para conseguir ese resultado?

Un integrante puede ser eficaz y no ser eficiente. Puede producir finalmente un buen resultado, pero requerir numerosas explicaciones, correcciones, reintentos y horas de coordinación humana. Ese costo también debe medirse.

Con el tiempo queremos poder observar cuánto trabajo realiza cada especialidad, cuánto tiempo requiere, cuánto esfuerzo humano necesita para ser coordinada, qué actividades generan retrabajo, qué roles aportan valor y cuáles generan más coordinación que beneficio.

También podremos analizar cuándo conviene combinar responsabilidades, incorporar una nueva especialidad, evolucionar una instancia o reemplazarla.

La propia estructura organizacional se convirtió así en parte del experimento.

---

# 14. La Project Manager también cambia su forma de trabajar

La evolución del modelo también modificó la función operativa de quien coordina LAPIN.

Al comienzo gran parte del trabajo consistía en interactuar directamente con una IA para resolver problemas. A medida que aparecieron especialistas, el trabajo comenzó a parecerse más a la gestión de una organización:

> **Necesidad → Especialista → Trabajo → Validación → Resultado → Medición**

La Project Manager comienza a funcionar cada vez más como orquestadora del sistema: identifica qué especialista necesita intervenir, asigna el trabajo, coordina dependencias, controla, valida, registra resultados, mide esfuerzo y utiliza esa información para mejorar el sistema.

Esto introduce otra métrica importante:

> **¿Cuánto esfuerzo humano requiere coordinar el equipo?**

El objetivo no es construir un equipo de Inteligencias Artificiales que necesite cada vez más trabajo humano para mantenerse funcionando. Si el modelo evoluciona correctamente, debería permitir obtener progresivamente más resultados con una coordinación razonable.

---

# 15. Empezamos a trabajar con un stack de Inteligencias Artificiales

Otra evolución importante ocurrió cuando dejamos de pensar que toda necesidad debía resolverse utilizando una única plataforma de Inteligencia Artificial.

Durante la generación de documentación apareció un caso concreto. Necesitábamos producir documentos utilizando templates visuales determinados. ChatGPT podía colaborar correctamente con el contenido, pero encontramos limitaciones para producir determinados resultados de formato.

Probamos entonces incorporar Claude al proceso y permitió resolver mejor esa necesidad utilizando el template definido.

Esto produjo otro aprendizaje:

> **No necesitamos encontrar una IA que sea la mejor para todo.**

Podemos utilizar un **stack de Inteligencias Artificiales especializadas** y elegir la herramienta que mejor resuelva cada necesidad.

Esto nos llevó a separar nuevamente conceptos:

- **Rol:** qué responsabilidad existe.
- **Proceso:** cómo realizamos el trabajo.
- **IA / herramienta:** qué tecnología utilizamos para ejecutarlo.

Hoy una actividad puede funcionar mejor con ChatGPT y otra con Claude. Mañana puede aparecer una herramienta mejor.

LAPIN debe poder incorporarla sin tener que rediseñar toda su organización.

Pero utilizar más herramientas tampoco significa automáticamente ser más eficientes. Cada incorporación puede introducir costos, aprendizaje, transferencia de contexto, mantenimiento e integraciones adicionales.

La herramienta debe aportar suficiente valor para justificar esa complejidad.

---

# 16. Las integraciones aumentan las capacidades de los integrantes

También descubrimos que el valor de una Inteligencia Artificial no depende solamente del modelo utilizado. Depende de las herramientas y del contexto a los que puede acceder.

Las integraciones de ChatGPT con herramientas de trabajo como correo electrónico y calendario mostraron nuevas posibilidades: revisar información, detectar mensajes importantes, consultar reuniones, preparar información antes de una reunión, generar minutas y documentos, realizar seguimientos, crear recordatorios y reducir tareas administrativas.

Esto permite comenzar a pensar en integrantes que no solamente reciben información manualmente, sino que pueden estar conectados, de manera controlada, con algunas de las herramientas necesarias para realizar su trabajo.

Esto podría reducir uno de los costos que estamos intentando medir:

> **El esfuerzo humano necesario para proporcionar contexto y coordinar a los integrantes.**

Pero también apareció una regla importante: no todos necesitan acceso a todo.

Las herramientas, integraciones y permisos deberían responder a las responsabilidades del puesto.

---

# 17. Primero entender, después automatizar

A medida que encontramos posibilidades de integración también comenzaron a aparecer oportunidades de automatización.

Pero decidimos no comenzar automatizando.

Primero necesitamos comprender el proceso, después comprobar que funciona, medirlo y recién entonces determinar qué partes tiene sentido optimizar o automatizar.

La secuencia que comenzó a aparecer dentro del laboratorio es:

> **Experimentar → Validar → Documentar → Medir → Optimizar → Automatizar**

Automatizar demasiado temprano puede significar simplemente ejecutar más rápido un proceso que todavía no sabemos si está correctamente diseñado.

Por eso el trabajo manual inicial también tiene valor: nos permite entender qué estamos haciendo antes de intentar eliminarlo.

---

# 18. La documentación se convirtió en memoria organizacional

A medida que aumentaban las decisiones apareció otro problema. No era razonable volver a explicar constantemente a cada integrante qué es LAPIN, cómo funciona, qué decisiones tomamos, qué aprendimos y qué reglas están vigentes.

La documentación comenzó entonces a cumplir una función mucho más importante. Dejó de ser solamente un registro y comenzó a convertirse en **memoria organizacional**.

GitHub permite conservar conocimiento de manera versionada y accesible. Esto reduce la dependencia de conversaciones individuales y de la memoria de una única persona.

Un integrante nuevo puede recibir documentación y comenzar a comprender la organización sin necesidad de reconstruir toda su historia mediante conversaciones.

La documentación también comenzó a formar parte de nuestra estrategia para reducir el costo de coordinación.

---

# 19. La documentación también necesitó especialización

Inicialmente incorporamos un Asistente de Redacción cuya función era principalmente mejorar textos y documentos.

Pero el crecimiento de LAPIN mostró que el problema era más amplio. No solamente necesitábamos escribir: necesitábamos organizar, estructurar, mantener, relacionar, simplificar, preservar y hacer reutilizable el conocimiento.

De esa necesidad nació **Knowledge & Documentation**.

Esto también mostró cómo un rol puede aparecer correctamente para resolver una necesidad inicial y posteriormente dejar de ser suficiente cuando la organización evoluciona.

---

# 20. Las reglas dispersas comenzaron a formar un Reglamento

Con el crecimiento del equipo fueron apareciendo reglas: cómo incorporar un integrante, cómo definir un puesto, qué hacer cuando algo está fuera de alcance, cómo evolucionar una instancia, cuándo darla de baja, cómo registrar el trabajo y cómo relacionarse con otros especialistas.

En un principio estas reglas aparecieron en documentos separados porque fueron descubiertas en momentos diferentes.

Con el tiempo detectamos que, en conjunto, estaban formando algo más grande: **un Reglamento de los Integrantes de LAPIN DIGITAL**.

Decidimos entonces consolidarlas y separar claramente cuatro tipos de documentación:

- **Reglamento de los Integrantes:** reglas comunes que debe cumplir cualquier Lapin.
- **Histórico de Integrantes:** quién formó parte de LAPIN, qué puesto ocupó, altas, bajas y motivos.
- **Evolución del modelo de Integrantes:** cómo llegamos hasta el modelo actual y qué aprendimos durante el proceso.
- **Legajos de Rol:** onboarding específico de cada puesto.

Esta separación busca evitar documentos duplicados y mantener una única responsabilidad para cada tipo de información.

---

# 21. El costo de aprender también forma parte del experimento

Llegar hasta el modelo actual consumió muchas horas de investigación, pruebas y error.

No todas las decisiones funcionaron. Probamos herramientas que posteriormente descartamos, creamos roles que resultaron demasiado limitados, reorganizamos documentación, evaluamos distintas formas de implementar integrantes, modificamos herramientas de gestión, incorporamos nuevas tecnologías y volvimos a analizar decisiones anteriores.

Muchas de estas actividades no produjeron inmediatamente un producto terminado.

Produjeron **conocimiento**.

Y ese conocimiento permitió que LAPIN comenzara a funcionar de una manera progresivamente más organizada.

Un experimento descartado no representa necesariamente tiempo perdido. Si permite evitar una decisión incorrecta, comprender mejor un problema o encontrar una solución más eficiente, genera conocimiento reutilizable.

Por eso también queremos registrar ese esfuerzo.

---

# 22. La organización también es un producto del laboratorio

Una parte importante del trabajo realizado hasta ahora no estuvo destinada a construir software. Estuvo destinada a construir **la organización capaz de producirlo**.

Actualmente LAPIN comienza a contar con integrantes especializados, responsabilidades y límites definidos, mecanismos de derivación, onboarding por puesto, un sistema de gestión, actividades registradas, tiempo medible, documentación organizada, memoria organizacional, diferentes herramientas de IA, integraciones con herramientas de trabajo y criterios para incorporar, evolucionar o dar de baja integrantes.

Esto permite que el trabajo comience a estar mejor orquestado.

Pero todavía necesitamos comprobar si puede sostenerse y escalar.

---

# Estado actual del experimento

Al **16/08/2026**, el modelo de Integrantes de LAPIN continúa en construcción y las decisiones actuales no se consideran definitivas.

Queremos comprobar si la organización puede mantener en el tiempo eficacia, eficiencia, calidad, especialización, coordinación, trazabilidad, capacidad de aprendizaje, capacidad de evolución y costos razonables de gestión.

Pasamos de conversar con Inteligencias Artificiales para resolver tareas individuales a comenzar a construir un sistema organizado de:

> **Personas + Inteligencias Artificiales + Roles + Herramientas + Conocimiento + Procesos + Medición**

Todavía no sabemos cuál será la estructura definitiva. Y justamente por eso seguimos documentando.

LAPIN HUB no pretende mostrar solamente aquello que terminó funcionando. Pretende conservar el camino: **qué necesitábamos, qué probamos, qué funcionó, qué descartamos, cuánto costó, qué aprendimos y por qué decidimos cambiar.**

Porque el objetivo no es solamente demostrar que podemos construir una organización utilizando Inteligencia Artificial.

El objetivo es determinar si podemos construir una organización que funcione de manera **eficaz, eficiente, medible y capaz de evolucionar**.