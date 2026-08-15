# Estructurar BACKLOG

## Informacion BETA a revisar


LAPIN HUB — Diseño y estructura de Jira

Documento de trabajo para definir la estructura de gestión de LAPIN HUB en Jira y registrar las decisiones que justifican su configuración.

1. Contexto

Organización: LAPIN DIGITAL
Proyecto: LAPIN HUB
Metodología: Scrum

LAPIN HUB es un proyecto de investigación, experimentación y documentación.

Que el proyecto incluya actividades de investigación, laboratorio o definición metodológica no cambia su naturaleza de proyecto.

Jira se utilizará para gestionar el trabajo de forma trazable, permitiendo identificar qué se planificó, qué se realizó, qué está pendiente y qué ocurrió durante cada Sprint.

Una característica particular del proyecto es que actualmente existe una única persona operando Jira, mientras que diferentes roles pueden ser ejecutados mediante IA, por la persona que orquesta el proyecto o, eventualmente, por otros integrantes.

2. Modelo general

La organización y los proyectos se entienden de la siguiente manera:

LAPIN DIGITAL
│
├── LAPIN HUB
│   └── Proyecto Scrum
│
├── LAPIN PEPE
│   └── Futuro proyecto
│
├── LAPIN ERP
│   └── Futuro proyecto
│
└── ...

LAPIN DIGITAL representa la organización.

LAPIN HUB representa un proyecto concreto dentro de la organización.

Los futuros proyectos podrán tener sus propias estructuras y metodologías según sus necesidades.

3. Usuarios y roles
3.1 Usuarios Jira

Un usuario Jira representa una cuenta real dentro de Jira.

Actualmente:

Usuarios Jira
└── Lapin Digital

Existe capacidad para incorporar más usuarios en el futuro, pero no se crearán usuarios artificiales para representar roles.

Decisión

Los roles no se representan mediante usuarios Jira.

Esto evita consumir usuarios disponibles simplemente para representar funciones organizacionales o agentes de trabajo.

3.2 Roles

Los roles representan qué función participa en la realización del trabajo.

Los roles son dinámicos y no constituyen una lista cerrada.

Un rol puede:

aparecer;
desaparecer;
modificarse;
dividirse;
combinarse;
ser ejecutado por IA;
ser ejecutado por una persona;
cambiar según la demanda del proyecto.

Ejemplos posibles:

Investigación
Desarrollo
Arquitectura
Documentación
QA
Análisis
etc.

Estos ejemplos no constituyen una taxonomía definitiva.

⭐ Decisión

Los roles se consideran una dimensión dinámica del sistema de trabajo y no usuarios de Jira.

4. ROL, Responsable y Etiquetas

Se diferencian tres conceptos que podrían confundirse:

Elemento	Para qué lo usamos	Ejemplos
ROL	Identificar el rol que participa en el trabajo	Investigación, Desarrollo, Arquitectura, QA
Etiqueta	Clasificar libremente la actividad	documentacion, analisis, investigacion, github
Responsable	Identificar al usuario Jira que gestiona/ejecuta la actividad	Lapin Digital
Sprint	Identificar el ciclo de trabajo	Sprint 01
Story Points	Estimar el esfuerzo relativo	1, 2, 3, 5, 8
Estado	Identificar la situación actual del trabajo	To Do, In Progress, In Review, Done
4.1 Campo ROL

El ROL se plantea como un campo estructurado y controlado.

Conceptualmente:

ROL
├── Investigación
├── Desarrollo
├── Arquitectura
├── Documentación
├── QA
└── ...

El catálogo podrá evolucionar con el proyecto.

⭐ Decisión

ROL debe representarse mediante un campo estructurado y no mediante una etiqueta.

Motivo

El rol representa una dimensión organizacional del trabajo que interesa consultar, filtrar y eventualmente medir.

Se busca poder responder preguntas como:

¿Qué trabajo realizó el rol Investigación?
¿Cuántos Story Points fueron asignados a Arquitectura?
¿Qué roles participaron en un Sprint?
¿Qué trabajo de un determinado rol permanece pendiente?

Un campo estructurado permite mantener consistencia y facilita este tipo de consultas.

4.2 Etiquetas

Las etiquetas tendrán una función diferente.

Ejemplos:

documentacion
analisis
investigacion
github
arquitectura
decision

Las etiquetas permiten incorporar contexto y clasificar actividades sin modificar la estructura principal de Jira.

⭐ Decisión

Las etiquetas se utilizarán como mecanismo de clasificación flexible y no como representación de roles.

Regla conceptual

ROL responde:

¿Qué rol participa en este trabajo?

Etiqueta responde:

¿Qué características o contexto tiene este trabajo?

Responsable responde:

¿Qué usuario de Jira gestiona la actividad?

5. Modelo Scrum

Jira no se utilizará simplemente como una lista de tareas.

LAPIN HUB utilizará un flujo basado en Scrum:

Product Backlog
       │
       ▼
Planificación del Sprint
       │
       ▼
Sprint Backlog
       │
       ▼
Trabajo
       │
       ▼
Incremento
       │
       ▼
Revisión / Retrospectiva
       │
       ▼
Nuevo Sprint

El objetivo es poder reconstruir el trabajo realizado durante cada ciclo.

6. Sprints

Inicialmente se utilizarán Sprints mensuales.

El objetivo es poder observar la evolución del sistema de trabajo a través del tiempo.

Cada Sprint deberá permitir identificar:

qué se planificó;
cuál era el Sprint Goal;
qué trabajo fue seleccionado;
qué se completó;
qué quedó pendiente;
qué se bloqueó;
qué se aprendió.
6.1 Velocidad

Se utilizarán Story Points para estimar el esfuerzo relativo de las actividades.

Ejemplo:

Sprint 01 → 23 puntos
Sprint 02 → 27 puntos
Sprint 03 → 25 puntos
Sprint 04 → 31 puntos

La velocidad se utilizará como una métrica para observar:

capacidad;
evolución;
previsibilidad;
comportamiento del equipo;
tendencia del sistema de trabajo.

No se considerará una medida absoluta de productividad.

7. Estructura de una Issue

La estructura buscada para una actividad es:

Issue
│
├── Tipo
├── Título
├── Descripción
├── ROL
├── Responsable
├── Estado
├── Prioridad
├── Sprint
├── Story Points
├── Etiquetas
└── Evidencia / enlaces

Cada campo debe tener una función concreta.

No se agregarán campos únicamente porque Jira los permita.

8. Features y Epics
Features

Inicialmente no se utilizarán Features.

No se incorporarán niveles de organización que no sean necesarios para el modelo actual.

Epics

Tampoco se definirá todavía una estructura cerrada de Epics.

Las agrupaciones futuras deberán surgir de las necesidades reales del proyecto.

⭐ Decisión

La estructura no se cerrará prematuramente.

Primero se observará cómo evoluciona el trabajo real de LAPIN HUB y luego se incorporarán niveles adicionales si aportan valor.

9. Workflow

El espacio actualmente presenta:

Backlog
   │
   ▼
To Do
   │
   ▼
In Progress
   │
   ▼
In Review
   │
   ▼
Done

Por ahora se mantendrá este flujo.

⭐ Decisión

Comenzar con un workflow simple y agregar estados únicamente cuando el trabajo real demuestre que son necesarios.

El objetivo es evitar una burocracia innecesaria.

10. Identificación del proyecto

Jira inicialmente había creado la clave:

SCRUM

Se decidió modificarla a:

LHB

Por lo tanto, las Issues se identifican como:

LHB-1
LHB-2
LHB-3
...
⭐ Decisión

La clave identifica al proyecto y no a la metodología.

SCRUM representa una metodología de trabajo y puede cambiar.

LHB identifica al proyecto LAPIN HUB.

Esto permite además mantener una convención consistente para futuros proyectos:

LHB-001 → LAPIN HUB
LPP-001 → LAPIN PEPE
LER-001 → LAPIN ERP
11. Categoría del espacio

Se configuró:

Categoría: Software

Esta configuración corresponde a la clasificación del espacio dentro de Jira.

No representa por sí misma una definición metodológica del proyecto.

12. Tipo de espacio

LAPIN HUB se configuró como:

Espacio de software gestionado por el equipo (Team-managed).

La configuración se realizará teniendo en cuenta las capacidades reales disponibles en esta modalidad y en Jira Free.

No se asumirán funcionalidades que no estén disponibles en la instancia utilizada.

13. Principio general de diseño

El principio que guía toda la configuración es:

No adaptar nuestra forma de trabajar a todas las opciones que Jira ofrece. Jira debe representar el sistema de trabajo que queremos construir.

Por lo tanto, cada nueva configuración deberá responder primero a una necesidad real.

La pregunta será:

¿Esto aporta valor al modelo de trabajo de LAPIN HUB?

Si no aporta valor, no se incorpora.

14. Separación de documentación

La documentación final se dividirá en dos partes.

14.1 Estructura y decisiones

Documento orientado a explicar:

Qué estructura se adoptó y por qué.

Incluirá decisiones como:

por qué LAPIN HUB es un proyecto;
por qué se utiliza Scrum;
por qué los roles no son usuarios;
por qué ROL es un campo estructurado;
por qué las etiquetas tienen otra función;
por qué se utiliza LHB;
por qué se mantiene un workflow simple;
por qué se utilizan Sprints mensuales;
por qué no se utilizan Features inicialmente;
por qué no se define todavía una estructura cerrada de Epics.

Este documento debe ser breve y orientado a decisiones, no un manual de Jira.

14.2 Configuración de Jira

Documento orientado a explicar:

Cómo se implementó la estructura en Jira.

Por ejemplo:

Crear espacio
      ↓
Seleccionar Scrum
      ↓
Configurar nombre
      ↓
Configurar clave LHB
      ↓
Configurar categoría
      ↓
Configurar campos
      ↓
Configurar tipos de trabajo
      ↓
Configurar workflow
      ↓
Configurar estimación
      ↓
Configurar Sprint
      ↓
Crear Product Backlog

Este documento podrá incluir capturas de pantalla cuando aporten valor.

15. Estado actual
Elemento	Estado
Proyecto	✅ LAPIN HUB
Metodología	✅ Scrum
Tipo de espacio	✅ Software / Team-managed
Clave	✅ LHB
Categoría	✅ Software
Usuario Jira	✅ 1 usuario
Roles	🟡 Por configurar
Campo ROL	🟡 Por configurar
Etiquetas	🟡 Por definir uso
Workflow	✅ Inicial
Story Points	🟡 Por configurar/validar
Sprint	🟡 Por configurar
Product Backlog	🟡 Por construir
Epics	⏸️ No definir todavía
Features	❌ No utilizar inicialmente
16. Decisiones de diseño registradas

Estas son las decisiones que actualmente consideramos de mayor importancia:

⭐ LAPIN HUB es un proyecto, aunque sea de investigación, experimentación y documentación.
⭐ Scrum es la metodología, no el nombre del proyecto.
⭐ Los roles no son usuarios Jira.
⭐ Actualmente existe un único usuario Jira.
⭐ Los roles son dinámicos y no constituyen una lista cerrada.
⭐ ROL se representa mediante un campo estructurado y filtrable.
⭐ Las etiquetas se utilizan para clasificación flexible.
⭐ Responsable representa al usuario Jira que gestiona la actividad.
⭐ Los Sprints serán inicialmente mensuales.
⭐ Story Points se utilizarán para estimación relativa y análisis de velocidad.
⭐ No se utilizarán Features inicialmente.
⭐ No se definirá todavía una estructura cerrada de Epics.
⭐ Se comenzará con un workflow simple.
⭐ LHB identifica al proyecto LAPIN HUB.
⭐ La configuración y las decisiones se documentarán por separado.
⭐ La complejidad se incorporará solamente cuando el trabajo real justifique su necesidad.
17. Principio de evolución

La estructura de Jira no se considera definitiva.

LAPIN HUB es también un espacio de experimentación sobre la forma de organizar y ejecutar trabajo con participación de IA.

Por lo tanto:

La estructura de gestión deberá evolucionar a partir de la experiencia real del proyecto.

Las nuevas necesidades, roles, estados, campos o agrupaciones se incorporarán cuando exista una razón concreta para hacerlo y, cuando corresponda, se registrará la decisión que motivó el cambio.