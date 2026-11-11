# Paso 2 — Reconocer Work Chains, Work Processes y Work Flows

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Comprender **qué trabajo reconoce la organización, cómo se articula y qué significado tienen sus relaciones**, utilizando [Work Chains](../concepts/work-chain.md), [Work Processes](../concepts/work-process.md) y [Work Flows](../concepts/work-flow.md) como conceptos de modelado.

Podemos comenzar **en cualquiera de los tres niveles**: aquel para el que tengamos suficiente evidencia y comprensión como para establecer una **isla de conocimiento estable**. Desde ella podemos ampliar el conocimiento hacia niveles superiores, inferiores o relacionados. Reconocer un nivel no requiere completar los demás, y los [actores reconocidos](01-reconocer-actores.md) pueden revisarse a medida que comprendemos el trabajo.

## Preguntas que orientan

- ¿Qué servicio, producción o responsabilidad motiva este conjunto de esfuerzos?
- ¿Desde qué Work Chain, Work Process o Work Flow podemos partir con suficiente conocimiento para sostener lo que afirmamos?
- ¿Cuál es el propósito y el resultado del [Work Process](../concepts/work-process.md)?
- ¿Qué acciones constituyen [Work Flows](../concepts/work-flow.md) **con significado propio** para la organización?
- ¿Qué relaciones, condiciones, alternativas o retornos existen entre esas acciones?
- ¿Qué decisiones pertenecen al proceso y cuáles al interior de una acción?
- ¿Qué relaciones, antecedentes, continuaciones o niveles de contexto conocemos realmente? ¿Dónde termina nuestra comprensión?
- ¿Qué es **desconocido**, y qué podemos afirmar con fundamento que **no existe**?

## Evidencia y límites

Contrastar cómo las personas **describen y realizan** el trabajo, procedimientos organizacionales, excepciones y casos observados. Las pantallas, endpoints, transiciones de estado y nombres de [Features](https://github.com/the-alive-lab/vslices/blob/main/products/framework/work.md) pueden aportar pistas, **pero no definen por sí mismos** el proceso organizacional.

Conservar la separación entre trabajo **actual**, trabajo **propuesto** y trabajo **deducido**. Si una representación de sistema no refleja el comportamiento organizacional, reconocer la discrepancia en lugar de ocultarla.

Distinguir explícitamente **conocimiento sustentado**, **desconocimiento** y **ausencia sustentada**. No saber qué antecede o sigue a un flujo, qué proceso lo contiene o qué cadena rodea un proceso **no implica que tales relaciones no existan**. Reconocer ese límite permite extender posteriormente la comprensión sin inventar continuidad ni aparentar completitud. No obliga a investigar inmediatamente todo lo que queda fuera.

## Cómo elaborar el modelo

1. **Elegir una isla de conocimiento suficientemente estable**: partir de una [Work Chain](../concepts/work-chain.md), un [Work Process](../concepts/work-process.md) o un [Work Flow](../concepts/work-flow.md), según dónde exista evidencia y claridad. No imponer una exploración de mayor a menor ni de menor a mayor.
2. **Comprender su significado y alcance**: qué trabajo representa, qué propósito o resultado reconocible tiene y cuáles de esas afirmaciones están sustentadas.
3. **Reconocer relaciones pertinentes**: otros niveles, acciones, condiciones, alternativas, retornos y consecuencias que la evidencia permita identificar, sin asumir secuencias o jerarquías completas.
4. **Delimitar dónde acaba nuestro conocimiento**: diferenciar los vínculos conocidos, los desconocidos y aquellos cuya ausencia podamos justificar. Esto incluye lo que podría existir antes, después o alrededor de lo estudiado.
5. **Extender la comprensión cuando aporte valor**: explorar relaciones hacia otras cadenas, procesos o flujos a partir de los límites reconocidos, sin completar niveles por obligación.
6. **Contrastar y revisar**: utilizar casos reales y discrepancias para confirmar, refinar o cuestionar tanto la isla conocida como sus límites.

Los conceptos distinguen niveles de significado, **no un orden obligatorio de descubrimiento**:

```text
Work Chain
  Work Process
    Work Flow
```

Un **[Work Flow](../concepts/work-flow.md)** es una acción semántica específica, no cualquier flecha ni un endpoint. Un [Work Process](../concepts/work-process.md) no equivale a una instancia de workflow administrada por un orquestador. Podemos comprender bien un Work Flow sin conocer todavía su proceso o cadena, y viceversa.

## Límites del nivel de comprensión

Una condición que relaciona acciones puede entenderse sin convertirla en una acción independiente. Cuando una decisión sea significativa a nivel del proceso, reconocerla como tal; si pertenece al comportamiento interno de un Work Flow, su examen puede quedar para una profundización posterior.

Mantener las acciones reconocidas independientes del vocabulario técnico de la implementación. Comprender la relación general entre acciones no exige resolver todavía todas sus entradas, decisiones internas y consecuencias específicas.

## Claridad esperada sobre el dominio

Deberíamos poder **explicar una porción reconocible del trabajo, su significado y las relaciones que conocemos**, identificando por qué nuestra comprensión es suficientemente estable como punto de apoyo para explorar otros niveles.

También deberíamos poder **señalar dónde termina nuestro conocimiento actual**: qué antecedentes, continuaciones o relaciones permanecen desconocidos, cuáles son hipótesis y qué ausencias podemos sostener con evidencia. **No conocer algo no equivale a que no exista**. Estos límites son parte del resultado del modelado, no errores que debamos ocultar o resolver inmediatamente.

La claridad no exige haber descubierto toda una [Work Chain](../concepts/work-chain.md), un [Work Process](../concepts/work-process.md) o todos sus [Work Flows](../concepts/work-flow.md), ni producir documentos, índices o diagramas.

**Cómo examinar la comprensión:** ¿podemos explicar desde dónde partimos y por qué ese conocimiento es confiable?, ¿distinguimos los niveles sin imponer una dirección de estudio?, ¿podemos indicar qué sabemos que antecede o sigue y qué desconocemos?, ¿evitamos convertir una relación desconocida en una ausencia afirmada?, ¿podría otra persona extender nuestra comprensión desde los límites identificados sin tener que adivinar qué asumimos?

## Ejemplo opcional para expresar el conocimiento

Un [Work Coordination Diagram](../../../products/docs-standard/diagramas/work-coordination-diagram.md) puede ayudar a **hacer visible la parte del trabajo que conocemos y sus relaciones**, pero no es necesario producirlo para alcanzar la claridad esperada.

En este paso todavía podríamos **no haber reconocido perfiles**. El siguiente ejemplo utiliza **un solo carril provisional, no un perfil organizacional definido**, exclusivamente como recurso de exposición: ilustra dos Work Flows y una relación secuencial, sin asignarles todavía responsabilidades.

```mermaid
---
config:
  theme: redux-color
---
swimlane-beta LR
    subgraph pendiente ["Perfil aún por reconocer (provisional)"]
        registrar["1. Registrar solicitud de soporte"]
        evaluar["2. Evaluar solicitud de soporte"]
    end

    registrar --> evaluar
```

Las acciones son una **selección parcial del caso de Serviu**, no un proceso que deba descubrirse siempre desde el inicio. El diagrama solo afirma aquí que conocemos esas dos acciones y su relación. No permite concluir que conozcamos todos sus antecedentes, continuaciones o perfiles. Tampoco establece que no existan otras acciones.

El carril provisional no debe confundirse con un [perfil](../concepts/profile.md) reconocido: una vez que conozcamos sus participaciones, podremos expresar esa comprensión en el [paso 4](04-relacionar-perfiles-con-work-flows.md). Las convenciones de lectura pertenecen a [Docs Standard](../../../products/docs-standard/diagramas/work-coordination-diagram.md), no a esta guía.

## Relación con los pasos siguientes

[Identificar perfiles](03-identificar-perfiles.md) examina quién realiza cada [Work Flow](../concepts/work-flow.md) y puede hacer visibles responsabilidades o acciones omitidas. Profundizar los [Work Flows](../concepts/work-flow.md) es un paso posterior aún sin guía especializada.

## Evidencia de referencia

[Work Process «Gestión de solicitud de soporte» en Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md). Su proceso concreto no se reproduce aquí ni se convierte en patrón obligatorio.
