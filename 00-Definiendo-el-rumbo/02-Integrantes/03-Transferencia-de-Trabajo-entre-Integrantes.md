> **Versión:** 1.0
> **Fecha:** 26/08/2026
> **Autor:** Jessica 

# Transferencia de Trabajo entre Integrantes

## Por qué surge este registro

A medida que una tarea pasa de un integrante a otro (handoff), el que la recibe necesita contexto rápido para arrancar sin tener que reconstruir la conversación anterior ni perder tiempo interpretando qué se hizo. Guardar ese contexto en Word, con formato prolijo pensado para lectura humana, agrega fricción: la mayoría de quienes leen estos archivos son integrantes IA, y un .md liviano se lee sin conversión ni ruido.

Además, este registro es distinto del que se lleva en GitHub Project: el Project registra la tarea (apertura, cierre, horas, trazabilidad de gestión). El handoff registra el **contexto operativo** que el siguiente integrante necesita para continuar — son dos cosas relacionadas pero no intercambiables.

## Decisión

Los handoffs se guardan como archivos `.md` en una carpeta de Dropbox dedicada (fuera de LAPIN HUB, porque son registros operativos de transferencia de trabajo, no conocimiento institucional permanente.).

### Convención de nombre

AAAA-MM-DD_NN_ROL-a-ROL_Titulo-breve.md


- **Fecha:** agrupa los handoffs cronológicamente, incluso cuando la carpeta crezca a lo largo de meses.
- **NN:** número secuencial que arranca en `01` cada día, para distinguir el orden entre varios handoffs del mismo día (una fecha sola no alcanza para eso).
- **ROL-a-ROL:** rol que entrega → rol que recibe, usando los códigos cortos ya definidos en LAPIN HUB (`DP`, `Tools`, `CEO`, `PM`, `Sr-DEV`, `UI-UX`, `Growth`, `K-D`), sin el prefijo `LD-` porque es redundante — todos los roles de LAPIN lo son.
- **Título breve:** el mismo criterio que ya usa el template de tarea de GitHub Project: corto y descriptivo, sin repetir la descripción.

**Ejemplo:** `2026-08-25_01_DP-a-PM_Revision-Identidad-y-Organizacion.md`

## Por qué esta convención y no otra

Se descartó usar solo un número secuencial sin fecha (tipo `000`, `001`...) porque, aunque ordena bien los handoffs dentro de un mismo día, pierde la referencia cronológica una vez que la carpeta crece — no permite saber de un vistazo si un handoff fue reciente o de hace semanas.

Se descartó también usar el nombre completo del rol (por ejemplo, "Documentation & Process") porque genera nombres de archivo largos y con caracteres problemáticos (como el `&`).

# TEMPLATE DE HANDOFF:

## Identificación

**Fecha:** Fecha de la elaboracion del handoff
**De:** código del Rol que entrega.
**Para:** código del Rol que debe continuar.
**Asunto:** descripción breve de la actividad que requiere continuidad.

---

## Contexto

Información mínima necesaria para comprender de dónde surge la necesidad y qué se estaba trabajando.

## Resultado generado

Qué resolvió o produjo el Integrante que entrega.

Incluir referencias a documentos, archivos o ubicaciones cuando corresponda.

## Actividad requerida

Qué necesita continuar el siguiente Integrante y qué se busca lograr.

No debe desarrollar la solución correspondiente al siguiente Rol.

## Consideraciones

Decisiones, restricciones, dependencias, riesgos o información relevante que el siguiente Integrante necesite conocer.

Si no existen, indicar **Ninguna**.