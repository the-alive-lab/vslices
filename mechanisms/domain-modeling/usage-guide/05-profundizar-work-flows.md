# Paso 5 — Profundizar los Work Flows

**Estado:** guía candidata, primera elaboración del 2026-11-10.  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Profundizar la comprensión de los [Work Flows](../concepts/work-flow.md) reconocidos, examinando **qué significa realizar cada acción para la organización**, en qué circunstancias ocurre, qué sucede durante ella y qué resultados y consecuencias produce.

En los pasos anteriores podemos haber reconocido las acciones, sus relaciones y los [perfiles](../concepts/profile.md) que participan. Aquí el foco cambia: **del lugar de una acción en el trabajo a su comportamiento y significado internos**. No buscamos todavía su realización técnica.

## Preguntas que orientan: seis perspectivas de comprensión

Estas perspectivas son **preguntas disponibles**, no partes obligatorias de una plantilla, una secuencia fija ni nuevos tipos de entidad. Podemos empezar por donde tengamos evidencia y profundizar hasta donde la pregunta de investigación lo justifique.

| Perspectiva | Pregunta orientadora |
|---|---|
| **Intención** | ¿Para qué existe este Work Flow? ¿Qué pretende conseguir dentro del trabajo? |
| **Activación** | ¿Qué circunstancias hacen que tenga sentido realizarlo? ¿Qué lo desencadena o habilita? |
| **Información** | ¿Qué necesita conocerse para realizar la acción y qué significado tiene esa información? |
| **Comportamiento** | ¿Qué ocurre dentro de la acción? ¿Qué decisiones, evaluaciones o transformaciones tienen significado organizacional? |
| **Resultado** | ¿Qué se obtiene, cambia o reconoce cuando se realiza? |
| **Consecuencias** | ¿Qué posibilidades, obligaciones, restricciones o trabajo posterior aparecen a partir de lo ocurrido? |

**Resultado y consecuencia son distintos:** lo que una acción produce no es necesariamente igual a lo que ese resultado habilita, exige o modifica en el resto del trabajo.

Ninguna perspectiva obliga a que el dominio tenga siempre una decisión, una transformación o una salida material. Cuando una pregunta no resulte pertinente o no sepamos responderla, distinguir ambas situaciones.

## Evidencia y límites de inferencia

Contrastar la comprensión con casos reales, descripciones organizacionales, procedimientos, excepciones y consecuencias observadas. Distinguir **lo observado, lo acordado, lo deducido o hipotético y lo desconocido**. Una observación de software puede aportar evidencia, pero no se convierte automáticamente en la definición de lo que hace la organización.

No suponer que conocemos todos los disparadores, alternativas o resultados por haber visto una ruta habitual. **No conocer una condición o consecuencia no equivale a afirmar que no existe**. Reconocer los límites del conocimiento permite continuar el estudio después, sin obligarnos a resolverlos todos ahora.

Separar este estudio de las decisiones de [System Realizations](../concepts/system-realizations.md): pantallas, endpoints, estados persistidos, [Features](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md), transacciones, permisos y mecanismos de orquestación no definen por sí mismos la semántica interna del Work Flow.

## Cómo examinar el dominio

1. **Elegir un Work Flow suficientemente reconocido**, con su significado y contexto conocidos hasta donde sea posible. No es necesario que todo su [Work Process](../concepts/work-process.md) o [Work Chain](../concepts/work-chain.md) esté completo.
2. **Establecer qué ya comprendemos** sobre su intención, relaciones y participación, y qué preguntas internas motivan profundizarlo. No repetir por ceremonia lo que ya está sustentado.
3. **Investigar las perspectivas pertinentes** desde la evidencia disponible. Podemos empezar por el resultado, las consecuencias o un caso excepcional si eso ofrece la isla de conocimiento más estable.
4. **Contrastar variantes y casos de frontera** para reconocer condiciones, decisiones y efectos que una descripción habitual podría ocultar, sin inventar ramas para completar un modelo.
5. **Distinguir los límites de la comprensión**: qué partes están sustentadas, cuáles permanecen hipotéticas y dónde continúa el desconocimiento.
6. **Revisar el alcance de lo estudiado** cuando aparezcan tensiones: una decisión interna puede seguir siendo parte de la acción, o la evidencia puede mostrar otra acción con significado propio. No descomponer automáticamente cada detalle en nuevos Work Flows.
7. **Conservar la comprensión alcanzada y continuar** hacia la pregunta siguiente cuando sea suficiente para el propósito actual, sin exigir exhaustividad ni artefactos documentales.

## Representar el comportamiento para comprenderlo y comunicarlo

Una representación gráfica puede ayudarnos tanto a **investigar relaciones que aún no comprendemos bien** como a **explicar con mayor claridad un comportamiento que ya conocemos**. Su aporte no depende exclusivamente de la dificultad, complejidad o incertidumbre del Work Flow: también puede hacer más legibles sus acciones internas, decisiones, alternativas, resultados y consecuencias para otras personas.

**Un Work Flow no requiere un diagrama por el hecho de existir.** Podemos optar por uno cuando una representación gráfica aporta claridad a lo que queremos examinar o comunicar; y podemos prescindir de él cuando la explicación actual cumple bien ese propósito. No se exige diagrama, notación única ni formato documental.

Distinguir los niveles que representamos:

- Un [Work Coordination Diagram](../../../products/docs-standard/diagramas/work-coordination-diagram.md) puede representar **cómo se relacionan los Work Flows y perfiles** en el nivel de coordinación del trabajo.
- Una representación **interna de un Work Flow**, cuando resulte pertinente, puede mostrar sus **acciones, decisiones, condiciones y resultados**, sin convertir automáticamente esos elementos en otros Work Flows ni en construcciones técnicas como `System Action`.
- Cuando el comportamiento interno muestra una continuación hacia **otro Work Flow**, distinguir la decisión que ocurre dentro de la acción de la **relación entre Work Flows** que corresponde al modelo del proceso. Podemos comunicar ambos aspectos sin duplicar sus autoridades conceptuales.

Por ejemplo, en el estudio de solicitudes de soporte, la distinción entre los alcances **Soporte** y **Mejora** se reconoce en **Evaluar solicitud de soporte** y determina su continuación hacia otros Work Flows. En **Supervisado y cierre de soluciones**, puede resultar esclarecedor representar cuándo se registra seguimiento y cuándo corresponde cerrar, siempre que se distingan las condiciones **ya comprendidas** de las que **todavía debemos contrastar**. En **Registrar solicitud de soporte**, un diagrama podría no aportar claridad adicional frente a una explicación suficiente.

Estos ejemplos **no prescriben diagramas concretos ni afirman condiciones internas aún no validadas**. La representación debe conservar el significado, las incertidumbres y los límites del conocimiento; **no completar ramas, decisiones o acciones por conveniencia gráfica**.

## Claridad esperada sobre el dominio

Deberíamos poder **explicar qué significa realizar el Work Flow, qué lo activa, qué sucede durante su realización, qué resultado produce y qué consecuencias tiene para el trabajo**, en la profundidad que permitan la evidencia y la pregunta estudiada.

También deberíamos poder **declarar qué desconocemos** y distinguir entre ausencia justificada y falta de conocimiento. Una comprensión útil puede ser parcial: no exige completar las seis perspectivas, estudiar todas las excepciones ni conocer ya cómo se implementará la acción.

**Cómo examinar la comprensión:** ¿podemos explicar la acción en términos del dominio sin recurrir a endpoints o pantallas?, ¿distinguimos resultado de consecuencia?, ¿sabemos qué decisiones pertenecen a la acción y cuáles podrían tener significado independiente?, ¿podemos justificar las condiciones que afirmamos?, ¿se reconocen los límites y la procedencia de lo comprendido?, ¿esta profundidad responde al objetivo de investigación?

## Revisión de pasos anteriores

La [guía general](README.md#orden-natural-y-revisión-entre-pasos) presenta los pasos en orden natural, **no irreversible**. Profundizar una acción puede revelar evidencia para revisar:

- El [paso 2](02-reconocer-procesos.md), si una acción antes considerada interna merece reconocerse como Work Flow independiente, cambia el límite del proceso o aparecen nuevas relaciones.
- El [paso 3](03-identificar-perfiles.md), si encontramos una función organizacional relevante que no estaba reconocida.
- El [paso 4](04-relacionar-perfiles-con-work-flows.md), si cambian las condiciones o responsabilidades de participación de algún perfil.
- El [paso 1](01-reconocer-actores.md), si la evidencia cuestiona nuestras distinciones entre posiciones de participación.

Volver a un paso anterior **no significa que el estudio previo haya sido inútil o incorrecto**: la nueva evidencia puede ampliar una comprensión que antes era suficientemente estable. Revisar solamente lo materialmente afectado, con coherencia respecto del objetivo general, y preservar cuando corresponda **comprensión anterior → evidencia o tensión → revisión → comprensión posterior**. Luego podemos retomar la profundización.

## Ejemplo de investigación: Registrar solicitud de soporte

En el [Work Process de gestión de solicitud de soporte de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md) reconocimos «Registrar solicitud de soporte» como acción semántica. **Las siguientes son preguntas, no respuestas validadas sobre Serviu:**

| Perspectiva | Pregunta para investigar |
|---|---|
| Intención | ¿Qué significa para Serviu registrar una solicitud? |
| Activación | ¿Cuándo y por qué alguien inicia una solicitud de soporte? |
| Información | ¿Qué antecedentes se necesitan para reconocer esa solicitud? |
| Comportamiento | ¿Qué evaluaciones o decisiones ocurren durante el registro? |
| Resultado | ¿Qué significa que la solicitud quede registrada? |
| Consecuencias | ¿Qué trabajo queda habilitado, pendiente o restringido después? |

Si descubrimos que una clasificación interna tiene significado organizacional independiente, **no la promovemos automáticamente a otro Work Flow**: contrastamos primero su significado y, si corresponde, revisamos el [paso 2](02-reconocer-procesos.md).

Este ejemplo no prescribe un formulario, una tabla obligatoria ni un documento propietario por acción; solo ilustra preguntas que podrían ayudar a profundizar la comprensión.

## Relación con los pasos siguientes

Lo comprendido puede orientar el estudio de [System Realizations](../concepts/system-realizations.md) sin convertirse en una correspondencia uno a uno ni en un diseño técnico anticipado. La sistematización puede revelar nueva evidencia y dar lugar a revisiones del propio Work Flow.

No es necesario profundizar **todos** los Work Flows antes de avanzar. Es suficiente disponer de conocimiento examinable y declarar sus límites para la decisión o investigación que sigue.
