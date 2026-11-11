# Guía de modelado de [Work Semantics](../concepts/work-semantics.md)

**Estado:** guía de uso candidata — 2026-11-10; primeros cinco pasos elaborados; sistematización posterior pendiente.  
**Mecanismo propietario de la orientación:** [Domain Modeling](../README.md).  
**Alcance:** comprender cómo una organización reconoce, organiza y coordina su trabajo, **antes** de decidir sus realizaciones de sistema. No es un estándar universal de diagramas ni un contrato de Framework.

## Propósito

Orientar el inicio de Domain Modeling mediante **[Work Semantics](../concepts/work-semantics.md)**, sin confundir procesos con estados del software, [actores](../concepts/actor.md) con cuentas o [perfiles](../concepts/profile.md) con permisos.

El primer movimiento no es diseñar funcionalidades de sistema: es **reconocer quiénes participan en el trabajo, qué procesos semánticos reconoce la organización y qué [perfiles](../concepts/profile.md) realizan sus acciones**.

## Recorrido inicial de modelado

### 1. Reconocer [actores](../concepts/actor.md)

[Guía detallada: reconocer actores](01-reconocer-actores.md). Identificar quiénes participan y desde qué posición contextual lo hacen, sin confundir [actor](../concepts/actor.md) con [participante](../concepts/participant.md), [perfil](../concepts/profile.md) o identidad técnica.

**Claridad esperada:** comprender quiénes participan, desde qué posiciones y cómo cambian según el contexto, distinguiendo lo conocido de lo hipotético.

### 2. Reconocer Work Chains, Work Processes y Work Flows

[Guía detallada: reconocer el trabajo y sus límites](02-reconocer-procesos.md). Partir de cualquiera de los tres niveles que permita establecer una **isla de conocimiento suficientemente estable**; comprender sus significados y relaciones sin imponer un orden de descubrimiento. Reconocer expresamente lo que sabemos, lo que desconocemos y las ausencias que podemos justificar.

**Claridad esperada:** comprender una porción del trabajo y sus relaciones con suficiente estabilidad para extender el conocimiento, **identificando dónde termina nuestra comprensión actual**, sin confundir desconocimiento con inexistencia.

### 3. Reconocer [perfiles](../concepts/profile.md) organizacionales

[Guía detallada: reconocer perfiles](03-identificar-perfiles.md). Comprender qué funciones y responsabilidades reconoce la organización y qué tipos de [actor](../concepts/actor.md) pueden desempeñarlas, sin exigir aún atribuirles acciones específicas.

**Claridad esperada:** comprender qué perfiles existen, qué significa cada uno y qué distinciones permanecen inciertas.

### 4. Relacionar [perfiles](../concepts/profile.md) con [Work Flows](../concepts/work-flow.md)

[Guía detallada: relacionar perfiles y Work Flows](04-relacionar-perfiles-con-work-flows.md). Examinar cómo participan los perfiles reconocidos en las acciones semánticas identificadas, qué responsabilidades ejercen y qué relaciones de participación podemos sostener. **No requiere un Work Process completo ni una notación específica.**

**Claridad esperada:** comprender qué perfiles intervienen en los Work Flows, de qué manera y bajo qué condiciones, identificando asignaciones sustentadas, candidatas y desconocidas.

### 5. Profundizar cada [Work Flow](../concepts/work-flow.md)

[Guía detallada: profundizar Work Flows](05-profundizar-work-flows.md). Examinar su **intención, activación, información, comportamiento, resultado y consecuencias**, partiendo de la evidencia disponible y sin exigir completar todas las perspectivas ni producir un formato documental.

**Claridad esperada:** comprender qué significa realizar la acción, qué ocurre en ella, qué produce y qué consecuencias tiene, reconociendo los límites de lo que aún desconocemos.

Una [Feature](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md) o una operación CRUD no demuestra por sí misma la existencia de un Work Flow autónomo.

### 6. Relacionar la comprensión con [System Realizations](../concepts/system-realizations.md)

Solo cuando exista una comprensión suficiente para tomar decisiones examinables, estudiar cómo sistematizar el trabajo. La elaboración comienza por **nombrar conceptos reconocibles** a partir del trabajo comprendido: información, comportamientos, invariantes, estados, perfiles, operaciones, capacidades u otros, sin exigir clasificarlos o formalizarlos de inmediato como construcciones de Framework.

En el **paso 6**, VSlices aporta por defecto **tres [burbujas de clasificación](../concepts/burbujas-de-clasificacion.md): [Space](https://github.com/vslices/lang-specification/blob/main/concepts/C-002-space.md), [Feature](https://github.com/vslices/lang-specification/blob/main/concepts/C-020-feature.md) y [Capability](https://github.com/vslices/lang-specification/blob/main/concepts/C-007-capability.md)**. Son categorías iniciales de exploración, **no capas, una lista exhaustiva ni una obligación de encajar cada concepto en una de ellas**. Quienes modelan pueden proponer otras burbujas —por ejemplo, las asociadas a un módulo, dominio o perfil— de acuerdo con las relaciones que descubran; pueden revisar las agrupaciones al volver sobre la comprensión previa.

La formación y revisión de burbujas examina [Coherencia](../concepts/coherencia.md) y [Cohesión](../concepts/cohesion.md) como **propiedades del modelo**, sin convertir una burbuja automáticamente en frontera técnica. Las fichas de Language Specification articulan Space, Feature y Capability para VSIR; la autoridad conceptual de esos conceptos permanece en VSlices Framework. La responsabilidad de **informar las burbujas iniciales y su uso metodológico pertenece a esta guía de Domain Modeling**, no a la documentación de cada proyecto que la aplica. El [Acoplamiento](../concepts/acoplamiento.md) queda reservado para la elaboración del paso 7.

Esta orientación del paso 6 sigue siendo **candidata**: su guía individual, así como las «organizaciones secuenciales» y los «divisores de significado», requieren todavía elaboración desde casos reales.

Consultar [Domain Modeling](../README.md) para la relación candidata `Work Flow → System Process` y la elaboración `System Process → System Action → System Step`. **No asumir mapeos uno a uno**.

La realización puede aportar evidencia que motive la revisión de [actores](../concepts/actor.md), [perfiles](../concepts/profile.md), procesos y flujos. Distinguir la comprensión anterior, la evidencia y la interpretación revisada, sin presentar la implementación como autoridad automática sobre el trabajo organizacional.

## Perspectivas transversales de comprensión

La investigación puede apoyarse en seis perspectivas: **intención** (para qué existe una acción), **activación** (en qué circunstancias se realiza), **información** (qué necesita conocerse), **comportamiento** (qué ocurre o se decide), **resultado** (qué cambia o se obtiene) y **consecuencias** (qué posibilidades, obligaciones o restricciones aparecen después).

**No son campos obligatorios, una nueva taxonomía del dominio ni una secuencia que debamos completar.** Cada paso recurre a las preguntas pertinentes según su responsabilidad y la evidencia disponible:

- **Paso 2:** reconocer acciones por su intención y resultado, y sus relaciones por las consecuencias que conocemos; las activaciones y condiciones pueden orientar dónde comienza o continúa el trabajo, sin profundizar todavía todo el comportamiento interno.
- **Paso 4:** reconocer por qué, cuándo y bajo qué condiciones interviene cada perfil, qué información necesita si la conocemos y qué responsabilidad ejerce respecto de las acciones y sus resultados.
- **Paso 5:** profundizar las seis perspectivas en el comportamiento del Work Flow, hasta donde el conocimiento y el propósito del estudio lo justifiquen.

**Resultado y consecuencia no son sinónimos**: obtener algo mediante una acción y habilitar trabajo posterior pueden ser hechos diferentes. Las perspectivas sirven para ampliar o revisar la comprensión, no para atribuir datos que todavía desconocemos.

## Orden natural y revisión entre pasos

Los pasos se presentan en un **orden natural de investigación**: el conocimiento obtenido en uno suele facilitar el siguiente. **No son etapas cerradas, ni su numeración prohíbe regresar a un paso anterior.**

Si durante cualquier paso aparece evidencia pertinente que amplía o cuestiona una comprensión previa, podemos **volver al paso afectado, revisar lo que corresponda y continuar**. Por ejemplo, al profundizar un [Work Flow](../concepts/work-flow.md) en el paso 5 podríamos reconocer otra acción semántica (revisar el paso 2), una función organizacional antes desconocida (paso 3) o una participación diferente (paso 4).

La revisión debe ser **coherente con la pregunta y el objetivo general del estudio**, sustentarse en lo descubierto y afectar solamente las distinciones que la evidencia realmente cuestiona. No hace falta rehacer todos los pasos ni completar artificialmente lo que seguimos desconociendo.

Cuando exista un cambio material en la interpretación, preservar la relación **comprensión anterior → nueva evidencia o tensión → revisión → comprensión posterior**, sin fingir que el conocimiento actualizado siempre estuvo disponible. Poder retomar un paso no transforma la guía en un procedimiento documental obligatorio ni altera la responsabilidad propia de cada paso.

## Criterio de las guías por paso

Cada paso distingue **propósito**, **preguntas para comprender**, **evidencia y límites de inferencia**, **cómo examinar el dominio**, **claridad esperada sobre el dominio** y **preguntas para revisar esa comprensión**.

La claridad alcanzada —no la producción de un documento, diagrama, catálogo, matriz o formato— es el resultado buscado. Las formas de representación, conservación y comunicación del conocimiento son **responsabilidades independientes de esta guía**. Pueden apoyar el examen, pero no determinan por sí solas si comprendemos el dominio.

Los pasos orientan la investigación, no son formularios obligatorios. Frente a desacuerdos o incertidumbres, evitar convertir una interpretación provisional en un hecho.

El paso 6 permanece esbozado en este índice; su guía individual está pendiente de elaboración desde evidencia adicional.

## Evidencia de referencia

El estudio de la ticketera de Serviu aportó evidencia para los primeros pasos: [actores](https://github.com/atom-dev-serviu/documentation/blob/main/actors/README.md), [gestión de solicitud de soporte](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md) y [perfiles](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/profiles/README.md). Son ejemplos para contrastar la guía, no formatos de documentación exigidos.

## Preguntas abiertas

- Cuánto detalle corresponde a un [Work Process](../concepts/work-process.md) o [Work Flow](../concepts/work-flow.md) en contextos distintos.
- Cuándo resulta útil formalizar más de un [perfil](../concepts/profile.md) [participante](../concepts/participant.md) o más de una responsabilidad por acción.
- Cómo representar variantes y condiciones sin imponer una notación universal.
- Qué otros conceptos de Domain Modeling requiere la evidencia más allá de este recorrido inicial de [Work Semantics](../concepts/work-semantics.md).

Esta guía describe un **recorrido natural, revisitable y no exhaustivo**; no afirma que los [actores](../concepts/actor.md), procesos o [perfiles](../concepts/profile.md) se descubran en un orden inmutable.
