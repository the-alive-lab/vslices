# Paso 4 — Relacionar perfiles con Work Flows

**Estado:** guía candidata, primera elaboración del 2026-11-10.  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Relacionar los [perfiles](../concepts/profile.md) reconocidos con los [Work Flows](../concepts/work-flow.md) identificados, comprendiendo **cómo participan las funciones organizacionales en las acciones semánticas del trabajo**.

Este paso combina la comprensión obtenida al [reconocer Work Chains, Work Processes y Work Flows](02-reconocer-procesos.md) con los perfiles [reconocidos anteriormente](03-identificar-perfiles.md). **No requiere partir de un Work Process completo** ni producir un diagrama, tabla, documento o conjunto de carriles.

## Preguntas que orientan

- ¿Qué perfiles intervienen en cada Work Flow conocido y en calidad de qué?
- ¿Quién realiza la acción, quién contribuye y quién responde por ella, cuando esa distinción sea pertinente y esté sustentada?
- ¿En qué condiciones participa cada perfil? ¿Puede intervenir más de uno?
- ¿Existen relaciones entre las participaciones que expliquen derivaciones, colaboraciones o cambios de responsabilidad?
- ¿Qué atribuciones están efectivamente comprendidas y cuáles todavía no conocemos?
- ¿La participación observada cuestiona nuestros perfiles o nuestra comprensión del Work Flow?

## Evidencia y límites de inferencia

Contrastar las participaciones con situaciones de trabajo, responsables organizacionales y evidencia disponible, distinguiendo **lo observado, lo acordado, las hipótesis y lo desconocido**.

**No deducir la asignación de un perfil por la semejanza entre su nombre y el verbo de una acción.** Que exista un «Agente de supervisión» no demuestra que participe en todas las acciones que se denominen «supervisar»; tampoco la existencia de un «Administrador» justifica asignarle cierres o aprobaciones.

Un [actor](../concepts/actor.md) y un [perfil](../concepts/profile.md) son distinciones diferentes. Tampoco se derivan de estas relaciones permisos, cuentas, cargos o responsabilidades técnicas.

El conocimiento puede ser **parcial**: que un Work Flow todavía no tenga un perfil conocido no lo invalida. La falta de asignación **no equivale** a que nadie participe; su límite debe quedar reconocido.

## Cómo examinar el dominio

1. **Elegir los Work Flows que comprendemos suficientemente**, sin requerir que toda su cadena o proceso esté completo. Conservar los límites conocidos y desconocidos del paso 2.
2. **Recuperar los perfiles reconocidos en su contexto**, sin crear perfiles solo para cubrir cada acción o etiqueta de un diagrama.
3. **Examinar la participación en cada acción**, distinguiendo ejecución, colaboración, responsabilidad u otras relaciones cuando tengan significado en ese trabajo. No imponer una categoría universal de participantes ni una cardinalidad fija.
4. **Examinar relaciones entre participaciones**: traspasos, colaboraciones, responsabilidades compartidas o condicionales, únicamente si la evidencia las sostiene.
5. **Distinguir asignaciones sustentadas, candidatas y desconocidas**, incluidas las condiciones bajo las cuales cambian. No rellenar silenciosamente los vacíos.
6. **Contrastar y revisar** los perfiles o los Work Flows si la participación real revela distinciones insuficientes o hipótesis equivocadas.

La operación conceptual es **relacionar perfiles con acciones semánticas**. En un caso concreto, puede ser útil mostrar esas relaciones sobre un Work Process mediante carriles, pero esa es una **proyección posible**, no la operación misma.

## Claridad esperada sobre el dominio

Deberíamos poder **explicar cómo intervienen los perfiles organizacionales en los Work Flows reconocidos**, qué responsabilidades ejercen, bajo qué condiciones y cómo se relacionan sus participaciones cuando el trabajo así lo requiere.

También deberíamos poder identificar **qué relaciones todavía desconocemos**, sin convertir una falta de evidencia en una ausencia de participación o en una atribución inventada. El resultado buscado es **comprensión**, independientemente de la forma de representarla o conservarla.

**Cómo examinar la comprensión:** ¿podemos justificar cada participación afirmada?, ¿sabemos distinguir un perfil de un actor o cuenta técnica?, ¿hemos atribuido responsabilidades por nombre o por evidencia?, ¿podemos reconocer dónde no sabemos quién participa?, ¿una nueva observación podría conducirnos a revisar el perfil o el Work Flow sin destruir las distinciones previas?

## Relación con los pasos siguientes

Este paso puede revelar preguntas internas de un Work Flow que merezcan profundización posterior. También puede cuestionar los perfiles del paso 3 o los límites conocidos del paso 2. La dirección de revisión no tiene que ser única.

No prescribe todavía la transformación hacia [System Realizations](../concepts/system-realizations.md), ni los contratos de autorización, ni la propiedad técnica de las acciones.

## Evidencia de referencia

En la [ticketera de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md), el Work Process ya representa dos asignaciones de perfil **candidatas**, mientras otras acciones tienen participación pendiente de determinar. El uso de carriles allí responde a la necesidad de examinar el caso; **no define cómo deben elaborarse todos los dominios**.

Las denominaciones de algunas acciones del diagrama de Serviu todavía difieren de su índice histórico de Work Flows. Esa diferencia debe resolverse con evidencia antes de atribuir responsabilidades definitivas.
