> **Versión:** 1.0  
> **Fecha:** Pendiente de confirmar  
> **Autor:** Jessica + LAPIN Knowledge & Documentation

# Experiencia de acceso de integrantes IA a archivos locales y remotos

## Por qué apareció la necesidad

Con la incorporación de VS Code y el trabajo sobre una copia local del repositorio LAPIN HUB, surgió una nueva necesidad: permitir que los integrantes IA accedieran a la documentación utilizada durante sus actividades.

Hasta ese momento, compartir archivos o enlaces era una forma de proporcionar contexto a los integrantes.

Sin embargo, a medida que aumentó la cantidad de documentos y las relaciones entre ellos, comenzó a resultar poco práctico proporcionar manualmente toda la información necesaria para cada tarea.

El objetivo era encontrar una forma de trabajar que permitiera consultar la documentación existente sin duplicarla ni generar operaciones innecesarias.

## Primera experiencia: acceso de ChatGPT a archivos locales

Se intentó utilizar ChatGPT para trabajar directamente con los archivos almacenados en una carpeta local de la PC.

La intención era que los integrantes IA pudieran consultar los documentos del repositorio local, sin necesidad de compartir cada archivo individualmente.

Durante la evaluación se exploraron alternativas para establecer ese acceso.

Sin embargo, en el entorno y la modalidad de trabajo utilizados, no se consiguió que ChatGPT accediera directamente a la carpeta local de Windows.

La búsqueda de una solución consumió más de una hora sin alcanzar el resultado esperado.

Esta experiencia dejó en evidencia un problema importante: **el tiempo invertido en intentar adaptar una herramienta también forma parte de su costo operativo.**

## El problema identificado

Durante la búsqueda de alternativas apareció una dificultad que ya habíamos experimentado al evaluar herramientas de gestión.

En lugar de comprobar rápidamente si una capacidad estaba disponible, se continuaban explorando posibles configuraciones y soluciones.

Aunque cada alternativa parecía razonable de manera individual, el conjunto terminó consumiendo demasiado tiempo para una necesidad concreta.

La experiencia permitió identificar que una herramienta puede resultar útil para muchas actividades y, aun así, presentar limitaciones para una operación específica.

No corresponde asumir que una capacidad existe únicamente porque sería conveniente disponer de ella.

Tampoco corresponde continuar indefinidamente buscando una solución cuando las condiciones reales de uso no permiten implementarla.

## Segunda experiencia: trabajo con Claude

También se utilizó Claude como integrante IA para trabajar con documentación de LAPIN.

En la configuración probada, Claude permitió acceder a carpetas locales de Windows.

Esto representaba una ventaja para consultar los documentos que se estaban editando mediante VS Code.

Sin embargo, durante la experiencia se encontraron dificultades para trabajar directamente con el repositorio remoto de GitHub.

Así apareció una situación particular:

- ChatGPT podía trabajar con documentación compartida mediante enlaces de GitHub, pero no se había conseguido el acceso directo a las carpetas locales.
- Claude podía trabajar con los archivos locales, pero el acceso al repositorio remoto no resultó igualmente práctico en la configuración utilizada.

Estas observaciones corresponden a las experiencias realizadas en ese momento y no constituyen afirmaciones sobre todas las capacidades de ambas plataformas.

## Solución operativa adoptada

En lugar de continuar intentando que ambas herramientas funcionaran de manera idéntica, se decidió aprovechar los mecanismos de acceso que ya habían resultado utilizables.

Para trabajar con ChatGPT, se utilizaron enlaces a documentos del repositorio de GitHub y archivos compartidos cuando fue necesario.

Para trabajar con Claude, se aprovechó el acceso a la carpeta local de Windows.

VS Code continuó siendo el entorno de edición local y Git el mecanismo de control de cambios y publicación.

De esta manera, no fue necesario modificar el modelo documental de LAPIN para adaptarlo a las particularidades de cada integrante IA.

La solución permitió continuar trabajando sin esperar a resolver todas las limitaciones de integración.

## Un problema adicional: documentación local y publicada

La utilización de archivos locales y documentos publicados introdujo una consideración importante.

Un documento modificado en la PC puede contener cambios que todavía no fueron publicados en GitHub.

Por lo tanto, el archivo local y su versión remota pueden presentar diferencias temporales.

Esto significa que dos integrantes IA podrían consultar contenidos diferentes si uno trabaja con la copia local y otro con el repositorio remoto.

Para evitar interpretaciones incorrectas, es necesario distinguir:

**Estado local:** documentos que pueden contener modificaciones pendientes de publicación.

**Estado publicado:** documentos disponibles en el repositorio remoto después del último push.

Esta diferencia debe tenerse en cuenta cuando se revisan documentos, se comparan resultados o se solicita la participación de distintos integrantes IA.

## Qué aprendimos

La experiencia permitió identificar varios aprendizajes:

### 1. Verificar las capacidades antes de diseñar una solución

Antes de dedicar tiempo a configurar una integración, es necesario comprobar si la herramienta puede realizar la operación requerida en las condiciones disponibles.

Una prueba pequeña puede evitar una investigación extensa que no conduzca a un resultado.

### 2. Reconocer las limitaciones reales

Cuando una capacidad no está disponible o no se consigue implementar, corresponde comunicarlo claramente.

Proponer alternativas es útil, pero no debe confundirse una posibilidad teórica con una solución comprobada.

### 3. No exigir que todas las herramientas funcionen igual

Los integrantes IA pueden disponer de diferentes mecanismos de acceso a la información.

El objetivo es que puedan realizar su trabajo, no que necesariamente utilicen las mismas interfaces o integraciones.

### 4. Considerar el tiempo como parte del costo

Una solución gratuita puede resultar costosa si requiere demasiado tiempo de configuración, investigación o mantenimiento.

La evaluación debe contemplar el esfuerzo necesario para obtener un resultado funcional.

### 5. Evitar dependencias innecesarias

El repositorio documental debe mantenerse organizado de manera que pueda utilizarse con distintas herramientas.

Cambiar de integrante IA o de plataforma no debería obligar a reconstruir el sistema documental.

### 6. Distinguir información local de información publicada

Antes de trabajar sobre un documento, es importante conocer si se está consultando su estado local o su última versión publicada.

Esto permite evitar revisiones basadas en información desactualizada.

## Criterio adoptado

A partir de esta experiencia se reforzó un criterio de evaluación:

**Primero comprobar que una solución funciona. Después invertir tiempo en optimizarla.**

Cuando aparece una necesidad tecnológica:

1. Identificar exactamente qué operación necesitamos realizar.
2. Verificar si la herramienta puede ejecutarla en nuestro entorno.
3. Realizar una prueba mínima.
4. Evaluar el tiempo, el costo y la complejidad.
5. Si no resulta viable, considerar alternativas sin modificar innecesariamente el modelo de LAPIN.
6. Documentar el resultado, incluso cuando la alternativa sea descartada.

Este criterio no implica abandonar una investigación ante la primera dificultad.

Implica reconocer cuándo el esfuerzo adicional deja de ser razonable frente al beneficio esperado.

## Decisión

Se decidió continuar utilizando los mecanismos de acceso que habían resultado prácticos:

- **ChatGPT:** documentación publicada en GitHub y archivos compartidos.
- **Claude:** documentación disponible en la carpeta local.
- **VS Code:** edición de documentos.
- **Git:** control de cambios y publicación.

No se consideró necesario resolver inmediatamente todas las diferencias de acceso entre las plataformas.

La solución podrá revisarse si aparecen nuevas capacidades, integraciones o necesidades operativas.

> **Una herramienta debe facilitar el trabajo de LAPIN. Si necesitamos invertir más esfuerzo en hacer funcionar la herramienta que en resolver el problema original, corresponde reconsiderar el camino.**

## Resultado de la experiencia

La investigación no produjo una integración única que permitiera a todos los integrantes IA trabajar de la misma manera sobre los archivos locales y remotos.

Sin embargo, permitió establecer una forma de trabajo viable, reconocer limitaciones concretas y evitar seguir invirtiendo tiempo en configuraciones que no habían dado resultado.

También reforzó una enseñanza que ya había aparecido durante la evaluación de Jira:

**No adaptar LAPIN a una herramienta cuando existen alternativas más simples para continuar avanzando.**

El aprendizaje obtenido pasa a formar parte de la experiencia tecnológica de LAPIN y podrá utilizarse en futuras evaluaciones de herramientas e integraciones.
