# Paso 2 — Reconocer los procesos semánticos de trabajo

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Comprender **qué trabajo reconoce y coordina la organización**, cuáles son los resultados que persigue y **qué acciones semánticas se relacionan** dentro de cada proceso. Este paso parte de los [actores reconocidos](01-reconocer-actores.md), pero permite revisar esa clasificación si aparecen nuevas formas de participación.

## Preguntas que orientan

- ¿Qué servicio, producción o responsabilidad motiva este conjunto de esfuerzos?
- ¿Qué cadena de trabajo lo contiene, y qué parte reconocible de ella estamos estudiando?
- ¿Cuál es el propósito y el resultado del [Work Process](../concepts/work-process.md)?
- ¿Qué acciones constituyen [Work Flows](../concepts/work-flow.md) **con significado propio** para la organización?
- ¿Qué relaciones, condiciones, alternativas o retornos existen entre esas acciones?
- ¿Qué decisiones pertenecen al proceso y cuáles al interior de una acción?

## Evidencia y límites

Contrastar cómo las personas **describen y realizan** el trabajo, procedimientos organizacionales, excepciones y casos observados. Las pantallas, endpoints, transiciones de estado y nombres de [Features](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md) pueden aportar pistas, **pero no definen por sí mismos** el proceso organizacional.

Conservar la separación entre trabajo **actual**, trabajo **propuesto** y trabajo **deducido**. Si un diagrama de sistema no refleja el comportamiento organizacional, registrar la discrepancia en lugar de ocultarla.

## Cómo elaborar el modelo

1. **Ubicar la cadena relevante ([Work Chain](../concepts/work-chain.md))**: qué trabajo conecta y qué límite del problema estudiaremos.
2. **Reconocer el [Work Process](../concepts/work-process.md)** por su intención y resultado, no por la cantidad de funciones o pantallas.
3. **Identificar [Work Flows](../concepts/work-flow.md) candidatos**: nombrar acciones por lo que significan para el trabajo (p. ej., «Registrar solicitud de soporte»), no por verbos CRUD o clases técnicas.
4. **Examinar relaciones entre acciones**: orden necesario, bifurcaciones significativas, retornos, condiciones y consecuencias. No asumir linealidad universal.
5. **Distinguir el nivel del proceso del nivel de cada acción**: comprender las relaciones significativas sin exigir conocer todas las decisiones internas de los Work Flows.
6. **Contrastar con un caso real** y revisar la descomposición cuando la evidencia no coincida.

Jerarquía candidata:

```text
Work Chain
  Work Process
    Work Flow
```

Un **[Work Flow](../concepts/work-flow.md)** es una acción semántica específica; **no** es el sinónimo de cualquier flecha en el diagrama ni un endpoint. Un [Work Process](../concepts/work-process.md) tampoco es una instancia de workflow administrada por un orquestador.

## Límites del nivel de comprensión

Una condición que relaciona acciones puede entenderse sin convertirla en una acción independiente. Cuando una decisión sea significativa a nivel del proceso, reconocerla como tal; si pertenece al comportamiento interno de un Work Flow, su examen puede quedar para una profundización posterior.

Mantener las acciones reconocidas independientes del vocabulario técnico de la implementación. Comprender la relación general entre acciones no exige resolver todavía todas sus entradas, decisiones internas y consecuencias específicas.

## Claridad esperada sobre el dominio

Al recorrer este paso, deberíamos poder **explicar qué trabajo reconoce la organización, para qué lo realiza, qué resultados busca y cómo relaciona sus acciones semánticas para alcanzarlos**. Deberíamos distinguir una cadena de trabajo de un proceso y una acción específica, reconocer relaciones y condiciones relevantes, y saber qué detalles todavía pertenecen al estudio de cada Work Flow.

Esa comprensión puede existir y examinarse sin producir índices, documentos ni diagramas. La ausencia de una representación particular no demuestra ausencia de comprensión; tampoco una representación completa demuestra por sí sola que sea correcta.

**Cómo examinar la comprensión:** ¿se puede explicar el proceso sin hablar de servicios o endpoints?, ¿cada [Work Flow](../concepts/work-flow.md) representa una acción reconocible?, ¿el diagrama mezcla pasos internos de otras acciones?, ¿las condiciones tienen respaldo?, ¿hay decisiones inventadas solo para completar el gráfico?

## Relación con los pasos siguientes

[Identificar perfiles](03-identificar-perfiles.md) examina quién realiza cada [Work Flow](../concepts/work-flow.md) y puede hacer visibles responsabilidades o acciones omitidas. Profundizar los [Work Flows](../concepts/work-flow.md) es un paso posterior aún sin guía especializada.

## Evidencia de referencia

[Work Process «Gestión de solicitud de soporte» en Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md). Su proceso concreto no se reproduce aquí ni se convierte en patrón obligatorio.
