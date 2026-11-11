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

**Claridad esperada:** comprender quiénes participan, desde qué posiciones y cómo cambian según el contexto, distinguiendo lo conocido de lo hipotético.

### 2. Reconocer los procesos semánticos de trabajo

[Guía detallada: reconocer procesos](02-reconocer-procesos.md). Identificar las cadenas, los procesos y los [Work Flows](../concepts/work-flow.md) que la organización reconoce, distinguiendo propósitos, resultados y relaciones entre acciones.

**Claridad esperada:** comprender qué trabajo realiza la organización, para qué lo hace y cómo coordina acciones semánticas para lograr sus resultados.

### 3. Identificar los [perfiles](../concepts/profile.md) de los [Work Flows](../concepts/work-flow.md)

[Guía detallada: identificar perfiles](03-identificar-perfiles.md). Examinar las responsabilidades y posiciones organizacionales que participan en cada [Work Flow](../concepts/work-flow.md); relacionarlas con [actores](../concepts/actor.md) sin derivar permisos técnicos.

**Claridad esperada:** comprender qué funciones y responsabilidades participan en cada acción, quiénes pueden desempeñarlas y dónde quedan incertidumbres.

### 4. Profundizar cada [Work Flow](../concepts/work-flow.md) por separado

Con el [Work Process](../concepts/work-process.md) y los [perfiles](../concepts/profile.md) reconocidos, profundizar la comprensión de cada [Work Flow](../concepts/work-flow.md): intención, disparador, [participantes](../concepts/participant.md), información necesaria, condiciones, decisiones internas, resultados y consecuencias observables.

Distinguir lo comprendido a nivel de proceso de aquello que requiere estudiar la acción concreta, sin imponer un formato para expresarlo.

El nombre de una [Feature](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md) o una operación CRUD no basta para demostrar que exista un [Work Flow](../concepts/work-flow.md) autónomo. Una acción que no cambia de etapa también puede tener significado de negocio.

### 5. Relacionar la comprensión con [System Realizations](../concepts/system-realizations.md)

Solo cuando exista una comprensión suficiente para tomar decisiones examinables, estudiar cómo sistematizar el trabajo. En esa elaboración pueden descubrirse **[Spaces](https://github.com/the-alive-lab/vslices/blob/main/products/framework/spaces.md), [Points](https://github.com/the-alive-lab/vslices/blob/main/products/framework/spaces.md), [Features](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md), [Capabilities](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md)**, restricciones y operaciones, mediante las definiciones y autoridades propias de VSlices.

Consultar [Domain Modeling](../README.md) para la relación candidata `Work Flow → System Process` y la elaboración `System Process → System Action → System Step`. **No asumir mapeos uno a uno**.

La realización puede aportar evidencia que motive la revisión de [actores](../concepts/actor.md), [perfiles](../concepts/profile.md), procesos y flujos. Distinguir la comprensión anterior, la evidencia y la interpretación revisada, sin presentar la implementación como autoridad automática sobre el trabajo organizacional.

## Criterio de las guías por paso

Cada paso distingue **propósito**, **preguntas para comprender**, **evidencia y límites de inferencia**, **cómo examinar el dominio**, **claridad esperada sobre el dominio** y **preguntas para revisar esa comprensión**.

La claridad alcanzada —no la producción de un documento, diagrama, catálogo, matriz o formato— es el resultado buscado. Las formas de representación, conservación y comunicación del conocimiento son **responsabilidades independientes de esta guía**. Pueden apoyar el examen, pero no determinan por sí solas si comprendemos el dominio.

Estos pasos son orientaciones revisables, no fases rígidas ni formularios obligatorios. Frente a desacuerdos o incertidumbres, evitar convertir una interpretación provisional en un hecho.

Los pasos 4 y 5 permanecen esbozados en este índice; sus guías individuales están pendientes de elaboración desde evidencia adicional.

## Evidencia de referencia

El estudio de la ticketera de Serviu motivó estos primeros pasos: [actores](https://github.com/atom-dev-serviu/documentation/blob/main/actors/README.md), [gestión de solicitud de soporte](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md) y [perfiles](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Son ejemplos para contrastar la guía, no formatos de documentación exigidos.

## Preguntas abiertas

- Cuánto detalle corresponde a un [Work Process](../concepts/work-process.md) o [Work Flow](../concepts/work-flow.md) en contextos distintos.
- Cuándo resulta útil formalizar más de un [perfil](../concepts/profile.md) [participante](../concepts/participant.md) o más de una responsabilidad por acción.
- Cómo representar variantes y condiciones sin imponer una notación universal.
- Qué otros conceptos de Domain Modeling requiere la evidencia más allá de este recorrido inicial de [Work Semantics](../concepts/work-semantics.md).

Esta guía describe el **primer recorrido de estudio**; no afirma que los [actores](../concepts/actor.md), procesos o [perfiles](../concepts/profile.md) se descubran en un orden inmutable.
