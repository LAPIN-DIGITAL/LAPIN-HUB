> **Versión:** 1.0  
> **Fecha:** Pendiente de confirmar  
> **Autor:** Jessica + LAPIN Knowledge & Documentation

# Trabajo local con VS Code y Git

## Contexto

A medida que avanzó la construcción de LAPIN DIGITAL, aumentó la cantidad de documentos que necesitábamos crear, revisar y mantener.

LAPIN HUB ya funcionaba como repositorio de conocimiento y GitHub Projects como sistema de gestión del trabajo.

Sin embargo, apareció una necesidad operativa: **trabajar sobre múltiples documentos de manera práctica, mantener su organización y publicar los cambios sin perder trazabilidad.**

## Incorporación de VS Code y el repositorio local

Se incorporó Visual Studio Code (VS Code) como entorno de edición de los documentos de LAPIN.

El repositorio Git permite trabajar con una copia local de LAPIN HUB, realizar modificaciones en los archivos Markdown y posteriormente publicar los cambios en GitHub.

Esto facilita:

- Trabajar directamente sobre la estructura de carpetas y archivos.
- Revisar y modificar varios documentos relacionados.
- Mantener los documentos en formato Markdown.
- Examinar los cambios antes de publicarlos.
- Agrupar modificaciones que corresponden a una misma actividad.

La edición local y la publicación de cambios se convirtieron en operaciones diferenciadas.

## Relación entre actividades y cambios documentales

Durante el trabajo se identificó la conveniencia de relacionar las modificaciones del repositorio con las actividades gestionadas en GitHub Projects.

Una misma actividad puede requerir modificar varios documentos.

Por ejemplo, revisar un procedimiento puede implicar actualizar también sus referencias en plantillas y documentos relacionados.

En lugar de publicar cada modificación por separado, se adoptó el criterio de **agrupar los cambios relacionados y asociar su publicación con la actividad correspondiente**.

De esta manera:

**GitHub Projects** identifica y permite seguir el trabajo.

**LAPIN HUB** conserva los documentos y sus resultados.

**Git** registra los cambios publicados en el repositorio.

Cada sistema aporta una dimensión diferente de la trazabilidad.

## Experiencia con el control de versiones

Durante las revisiones documentales apareció una dificultad: las versiones declaradas dentro de los archivos no siempre coincidían con la secuencia de modificaciones y publicaciones realizadas mediante Git.

Esto permitió distinguir dos conceptos:

### Versión documental

Identifica una edición del contenido de un documento.

Se declara explícitamente en sus metadatos y permite reconocer la evolución de ese contenido.

### Commit de Git

Registra un conjunto de modificaciones realizadas en el repositorio.

Un commit puede incluir varios documentos y no necesariamente representa una nueva versión individual de cada uno.

La relación entre ambos conceptos requiere un criterio consistente.

## Problema detectado

Durante el trabajo de revisión, varios documentos podían modificarse localmente antes de realizar un commit.

Si se incrementaba la versión documental en cada ajuste intermedio, podían aparecer versiones que nunca habían sido publicadas como estados independientes.

Por ejemplo:

`v3.0 → v3.1 → v3.2 → v3.3`

Si todos esos ajustes se realizaban antes de una única publicación, las versiones intermedias no representaban necesariamente documentos que hubieran existido como entregables publicados.

Esto dificultaba interpretar el historial documental y relacionarlo con el historial de Git.

## Criterio adoptado

Se estableció que **la versión documental debe revisarse antes de publicar los cambios**, tomando como referencia la última versión efectivamente publicada.

Los ajustes realizados durante una misma etapa de edición no requieren incrementos sucesivos de versión.

Antes de realizar un commit corresponde:

1. Revisar qué documentos fueron modificados.
2. Compararlos con sus últimas versiones publicadas.
3. Determinar si corresponde actualizar sus versiones documentales.
4. Comprobar la consistencia de los metadatos.
5. Verificar referencias y enlaces afectados por cambios de nombres o ubicaciones.
6. Agrupar los cambios relacionados con la actividad realizada.
7. Publicarlos mediante Git.

Este criterio permite conservar una relación más clara entre los documentos y su historial de modificaciones.

## Movimiento y reorganización de archivos

Otra necesidad identificada fue mantener la integridad de las referencias cuando se reorganizan carpetas o documentos.

Mover o renombrar un archivo no implica únicamente cambiar su ubicación.

También puede afectar enlaces desde otros documentos, referencias a procedimientos y rutas utilizadas en plantillas.

Por eso, la reorganización debe contemplar la revisión de las referencias entrantes y salientes antes de publicar los cambios.

El objetivo es evitar que una mejora en la organización produzca inconsistencias en el sistema documental.

## Qué aprendimos

La experiencia permitió identificar varios aprendizajes:

- La edición local facilita revisar documentos relacionados.
- GitHub Projects y Git cumplen funciones complementarias, pero diferentes.
- Una actividad puede producir cambios en múltiples archivos.
- No es necesario realizar un commit por cada ajuste menor.
- Las versiones documentales y los commits no son equivalentes.
- Incrementar versiones durante cada edición puede generar historiales inconsistentes.
- La revisión previa a la publicación permite detectar errores de versiones, rutas y referencias.
- El control de versiones debe aportar trazabilidad sin convertirse en una carga administrativa innecesaria.

## Decisión

Se adoptó el trabajo local con VS Code y Git como mecanismo operativo para mantener la documentación de LAPIN HUB.

Los cambios relacionados pueden agruparse en commits asociados a las actividades gestionadas.

La versión de cada documento se determina a partir de su última versión publicada y de la naturaleza de los cambios realizados.

Antes de publicar, se revisan versiones, metadatos, movimientos de archivos y referencias documentales.

> **El objetivo del control de versiones no es multiplicar números ni commits, sino poder reconstruir qué cambió, por qué cambió y en qué momento se publicó.**

## Continuidad de la experiencia

El trabajo local resolvió parte de las necesidades de edición y organización documental.

Sin embargo, al incorporar distintos integrantes IA al proceso aparecieron nuevas dificultades relacionadas con el acceso a los archivos locales y remotos.

Estas experiencias corresponden a una etapa posterior, que se documentará por separado.
