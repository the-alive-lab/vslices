# Guía de modelado de [Work Semantics](../concepts/work-semantics.md)

**Estado:** guía de uso candidata — 2026-11-10; primeros tres pasos elaborados; pasos posteriores pendientes.  
**Mecanismo propietario de la orientación:** [Domain Modeling](../README.md).  
**Alcance:** comprender cómo una organización reconoce, organiza y coordina su trabajo, **antes** de decidir sus realizaciones de sistema. No es un estándar universal de diagramas ni un contrato de Framework.

## Propósito

Orientar el inicio de Domain Modeling mediante **[Work Semantics](../concepts/work-semantics.md)**, sin confundir procesos con estados del software, [actores](../concepts/actor.md) con cuentas o [perfiles](../concepts/profile.md) con permisos.

El primer movimiento no es diseñar funcionalidades de sistema: es **reconocer quiénes participan en el trabajo, qué procesos semánticos reconoce la organización y qué [perfiles](../concepts/profile.md) realizan sus acciones**.

## Recorrido inicial de modelado

### 1. Reconocer [actores](../concepts/actor.md)

[Guía detallada: reconocer actores](01-reconocer-actores.md). Identificar quiénes participan y desde qué posición contextual lo hacen, sin confundir [actor](../concepts/actor.md) con [participante](../concepts/participant.md), [perfil](../concepts/profile.md) o identidad técnica.

**Resultado:** tipos de [actor](../concepts/actor.md) reconocibles y sus fuentes, con incertidumbres explícitas.

### 2. Reconocer los procesos semánticos de trabajo

[Guía detallada: reconocer procesos](02-reconocer-procesos.md). Identificar las cadenas, los procesos y los [Work Flows](../concepts/work-flow.md) que la organización reconoce, distinguiendo propósitos, resultados y relaciones entre acciones.

**Resultado:** procesos navegables y acciones semánticas candidatas, con sus relaciones justificadas.

### 3. Identificar los [perfiles](../concepts/profile.md) de los [Work Flows](../concepts/work-flow.md)

[Guía detallada: identificar perfiles](03-identificar-perfiles.md). Examinar las responsabilidades y posiciones organizacionales que participan en cada [Work Flow](../concepts/work-flow.md); relacionarlas con [actores](../concepts/actor.md) sin derivar permisos técnicos.

**Resultado:** [perfiles](../concepts/profile.md) contextualizados y relaciones con [actores](../concepts/actor.md) y acciones, diferenciando asignaciones comprobadas y pendientes.

### 4. Profundizar cada [Work Flow](../concepts/work-flow.md) por separado

Con el [Work Process](../concepts/work-process.md) y los [perfiles](../concepts/profile.md) reconocidos, elaborar **un documento propietario por [Work Flow](../concepts/work-flow.md)**. Examinar su intención, disparador, [participantes](../concepts/participant.md), información necesaria, condiciones, decisiones internas, resultados y consecuencias observables.

No repetir el diagrama general del proceso dentro de cada [Work Flow](../concepts/work-flow.md). Enlazar al proceso padre, al [perfil](../concepts/profile.md) correspondiente y a las fuentes que justifican el significado de la acción.

El nombre de una [Feature](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md) o una operación CRUD no basta para demostrar que exista un [Work Flow](../concepts/work-flow.md) autónomo. Una acción que no cambia de etapa también puede tener significado de negocio.

### 5. Relacionar la comprensión con [System Realizations](../concepts/system-realizations.md)

Solo cuando exista una comprensión suficiente para tomar decisiones examinables, estudiar cómo sistematizar el trabajo. En esa elaboración pueden descubrirse **[Spaces](https://github.com/the-alive-lab/vslices/blob/main/products/framework/spaces.md), [Points](https://github.com/the-alive-lab/vslices/blob/main/products/framework/spaces.md), [Features](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md), [Capabilities](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md)**, restricciones y operaciones, mediante las definiciones y autoridades propias de VSlices.

Consultar [Domain Modeling](../README.md) para la relación candidata `Work Flow → System Process` y la elaboración `System Process → System Action → System Step`. **No asumir mapeos uno a uno**.

La realización puede aportar evidencia que motive la revisión de [actores](../concepts/actor.md), [perfiles](../concepts/profile.md), procesos y flujos. Registrar **posición anterior → evidencia → revisión → posición posterior** sin presentar la implementación como autoridad automática sobre el trabajo organizacional.

## Estructura compartida de las guías por paso

Los documentos de los tres primeros pasos distinguen **propósito**, **preguntas para comprender**, **evidencia y límites de inferencia**, **forma de elaborar el modelo**, **resultado examinable** y **criterios para revisar**. No son formularios obligatorios ni fases cerradas. Ante desacuerdos, conservar las interpretaciones y su procedencia hasta resolverlos.

Los pasos 4 y 5 permanecen descritos de forma inicial en este índice; **sus guías individuales están pendientes** de elaboración a partir de evidencia adicional. No interpretar su ausencia como retiro conceptual.

## Convenciones de representación

Un diagrama es una **proyección de un modelo**, no el modelo mismo.

Para un [Work Process](../concepts/work-process.md) puede usarse un diagrama de actividades con **carriles por [perfil](../concepts/profile.md)** si se conoce quién actúa y el renderizador lo soporta. `swimlane-beta` con `redux-color` en Mermaid es una opción visual **comprobada para el caso de documentación de Serviu en GitHub (2026-11-10)**, no una obligación técnica o conceptual para VSlices.

El diagrama debería conservar acciones semánticas, relaciones y condiciones relevantes. **No confundir tipos de [actor](../concepts/actor.md) (p. ej. interno/externo) con [perfiles](../concepts/profile.md) ejecutores**. No introducir carriles de [perfiles](../concepts/profile.md) ficticios como si fueran definiciones organizacionales aprobadas; marcar expresamente la incertidumbre cuando haga falta.

Las notaciones, colores y configuración del renderizador pueden cambiar sin cambiar el significado del trabajo.

## Organización documental y trazabilidad

- **Índices / README de ámbito:** orientan hacia documentos propietarios; no duplican diagramas, listas detalladas ni definiciones.
- **[Actores](../concepts/actor.md):** tipos de participación, con su procedencia y clasificación contextual.
- **Perfiles:** catálogo contextual y una definición por [perfil](../concepts/profile.md); relacionan tipos de [actores](../concepts/actor.md) y responsabilidades sin asumir permisos.
- **Procesos:** documento propietario de cada [Work Process](../concepts/work-process.md) y su representación general.
- **[Work Flows](../concepts/work-flow.md):** documentos propietarios de cada acción semántica, referenciados desde el proceso.
- **Evidencia técnica:** separar los comportamientos de sistema observados de las definiciones del trabajo.

Al crear o revisar documentos, registrar fuentes, fecha de observación si importa, decisiones acordadas, hipótesis y preguntas abiertas. Conservar enlaces y trayectoria de cambios en Git. Una decisión no se vuelve verdadera por aparecer en un diagrama.

## Ejemplo de referencia sin duplicación

En Serviu se inició por tipos de [actores](https://github.com/atom-dev-serviu/documentation/blob/main/actors/README.md), luego el [Work Process de gestión de solicitud de soporte](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md), y se estableció un catálogo contextual de [perfiles de ticketera](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Sus [Work Flows](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/flows/README.md) serán profundizados por separado.

Este caso es **evidencia para revisar la guía**, no una definición obligatoria de todos los dominios ni una copia de sus diagramas.

## Preguntas abiertas

- Cuánto detalle corresponde a un [Work Process](../concepts/work-process.md) o [Work Flow](../concepts/work-flow.md) en contextos distintos.
- Cuándo resulta útil formalizar más de un [perfil](../concepts/profile.md) [participante](../concepts/participant.md) o más de una responsabilidad por acción.
- Cómo representar variantes y condiciones sin imponer una notación universal.
- Qué otros conceptos de Domain Modeling requiere la evidencia más allá de este recorrido inicial de [Work Semantics](../concepts/work-semantics.md).

Esta guía describe el **primer recorrido de estudio**; no afirma que los [actores](../concepts/actor.md), procesos o [perfiles](../concepts/profile.md) se descubran en un orden inmutable.
