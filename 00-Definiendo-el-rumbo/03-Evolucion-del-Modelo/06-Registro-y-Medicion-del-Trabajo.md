> **Versión:** 1.0
> **Fecha:** 07/11/2026
> **Autor:** Jessica +RRHH + DP

# Registro y Medición del Trabajo

**Estado:** Propuesta en análisis  
**Ámbito:** Evolución del Modelo LAPIN

## 1. Contexto

LAPIN DIGITAL trabaja con un modelo de Integrantes especializados, humanos o basados en inteligencia artificial.

Cada Integrante desarrolla actividades dentro de su especialidad, registra sus tareas y documenta los resultados obtenidos.

Durante la evaluación del registro de horas surgió una necesidad adicional: **no alcanza con conocer cuántas horas se dedicaron a una tarea; necesitamos comprender cómo se distribuyó ese tiempo y qué participación tuvieron las personas y la IA.**

Esta reflexión surge también de la experiencia de registrar horas manualmente en Excel y de la iniciativa de construir LAPIN Time Tracker.

## 2. Origen de la reflexión

Inicialmente se planteó registrar el tiempo mediante instrucciones sencillas durante la interacción con un Integrante:

- **Iniciamos:** registrar el comienzo del trabajo.
- **Paramos:** registrar una pausa.
- **Seguimos:** registrar la reanudación.
- **Cerramos:** finalizar el registro y calcular la duración.

La posibilidad de registrar estos eventos permitiría reconstruir las sesiones de trabajo vinculadas a una tarea.

Aunque actualmente los Integrantes no operan necesariamente como agentes autónomos capaces de guardar sus propios registros, este mecanismo podría servir como antecedente para una futura automatización.

## 3. Evolución de la idea

### 3.1. Contrastar los registros

Se identificó la posibilidad de contar con dos fuentes de información:

- **Tiempo declarado:** horas informadas por la persona en el Time Tracker.
- **Tiempo registrado:** períodos de actividad documentados durante la ejecución del trabajo.

Por ejemplo, una persona declara 10 horas mientras que los registros disponibles reflejan 3 horas de actividad.

Esta diferencia no demuestra necesariamente 7 horas improductivas. Puede corresponder a investigación, análisis, trabajo fuera del entorno registrado o períodos sin seguimiento.

Sin embargo, permite identificar diferencias que requieren revisión.

### 3.2. Identificar el tipo de actividad

Se observó que registrar únicamente la duración total de una tarea resulta insuficiente.

Una misma tarea puede involucrar:

- Investigación.
- Análisis.
- Desarrollo manual.
- Desarrollo asistido por IA.
- Pruebas y correcciones.
- Documentación.
- Coordinación.
- Pausas o interrupciones.

La clasificación permitiría conocer en qué actividades se invierte el tiempo.

**Una actividad no necesariamente requiere una tarea independiente.** La separación debe responder a objetivos y entregables reales, evitando multiplicar tareas artificialmente.

### 3.3. Diferenciar trabajo humano y trabajo de IA

La reflexión derivó en una distinción fundamental:

**El tiempo de trabajo humano no equivale al tiempo de ejecución de una IA.**

Se identifican tres dimensiones:

| Dimensión | Descripción |
|---|---|
| Tiempo humano | Esfuerzo dedicado por una persona. |
| Tiempo de IA | Duración de la ejecución o procesamiento de la IA. |
| Tiempo transcurrido | Período total desde el inicio hasta la finalización, incluyendo esperas e interrupciones. |

Estas dimensiones pueden superponerse y no deben sumarse automáticamente.

Además, una conversación con IA no constituye por sí sola una medición precisa del tiempo de procesamiento de la IA.

### 3.4. Diferenciación entre estimación y registro horario

Durante la actualización del Template de tarea surgió la necesidad de distinguir dos conceptos:

- **Tiempo estimado:** duración prevista para completar una tarea.
- **Fecha y hora de inicio:** momento real en que comienza su ejecución.

Inicialmente se consideró incorporar únicamente el tiempo estimado. Sin embargo, se identificó que este dato no permite calcular la duración real del trabajo.

Por ello, se decidió registrar ambos valores en la Apertura y agregar la fecha y hora de finalización en el Cierre.

Esta diferenciación permite:

- Comparar el esfuerzo previsto con el real.
- Calcular tiempos transcurridos.
- Identificar desviaciones.
- Mejorar futuras estimaciones utilizando información histórica.

**Decisión adoptada:** incorporar ambos campos al Template de tarea v2.1, sin modificar el Reglamento general ni duplicar instrucciones operativas.

## 4. Valor para el Modelo LAPIN

La información obtenida podría utilizarse para:

1. **Mejorar las estimaciones:** utilizar tiempos históricos reales según Rol, actividad y modalidad de trabajo.
2. **Evaluar eficiencia:** comparar esfuerzo humano, ejecución de IA y resultados obtenidos.
3. **Identificar oportunidades de mejora:** detectar retrabajos, investigaciones prolongadas, esperas y costos de coordinación.
4. **Evaluar la incorporación de IA:** determinar si la asistencia o automatización reduce efectivamente el esfuerzo humano.
5. **Mejorar la trazabilidad:** relacionar tareas, actividades, tiempos y resultados.
6. **Conciliar registros:** identificar diferencias entre tiempos declarados y evidencias disponibles.

El objetivo no es únicamente controlar horas, sino **comprender el costo real del trabajo y mejorar el funcionamiento del modelo organizacional**.

## 5. Limitaciones identificadas

- El registro de una conversación no demuestra actividad humana continua.
- Una sesión abierta no equivale necesariamente a tiempo trabajado.
- El tiempo de respuesta de una IA no representa todo el esfuerzo asociado a utilizarla.
- Pueden existir actividades legítimas fuera del entorno de registro.
- Los registros deben conservarse en un sistema persistente para permitir seguimiento y auditoría.
- Las diferencias entre registros no deben interpretarse automáticamente como improductividad.

## 6. Propuesta surgida de la investigación

Se propone evolucionar hacia un modelo donde cada Integrante pueda registrar sus sesiones de trabajo y asociarlas a las tareas correspondientes.

El registro debería permitir distinguir actividades, pausas, participación humana y ejecución de IA, según las capacidades disponibles.

En una etapa futura, los agentes podrían generar y guardar automáticamente registros vinculados a sus tareas, reduciendo la intervención manual.

La información resultante serviría como insumo para LAPIN Time Tracker, la planificación y la evaluación del modelo.

## 7. Separación entre investigación y normativa

Este documento conserva el razonamiento, las oportunidades y las limitaciones identificadas.

Las instrucciones obligatorias para los Integrantes deberán definirse en:

**02-Integrantes/01-Reglamento-de-Integrantes.md**

Los requerimientos funcionales y técnicos de LAPIN Time Tracker deberán gestionarse por los Roles responsables del producto y su implementación.

## 8. Aspectos pendientes de definición

- Qué eventos y actividades será obligatorio registrar.
- Cómo se identificará el tiempo humano frente al tiempo de IA.
- Qué mecanismos permitirán guardar y recuperar registros.
- Cómo se conciliará la información con LAPIN Time Tracker.
- Qué criterios utilizará RRHH para interpretar diferencias.
- Cómo se implementará progresivamente sin generar carga administrativa innecesaria.

## 9. Conclusión

La reflexión comenzó como una alternativa para simplificar el registro manual de horas y evolucionó hacia una oportunidad de medir el funcionamiento del Modelo LAPIN.

**Registrar tiempo no debe convertirse en un fin en sí mismo.**

Su verdadero valor está en generar información confiable para estimar mejor, reducir esfuerzo innecesario, evaluar la contribución de la IA y tomar decisiones sobre la evolución de la organización.