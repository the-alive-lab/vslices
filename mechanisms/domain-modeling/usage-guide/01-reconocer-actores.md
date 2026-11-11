# Paso 1 — Reconocer [actores](../concepts/actor.md)

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Reconocer **quiénes participan en el trabajo y desde qué posición contextual lo hacen**, antes de describir sus responsabilidades específicas en cada [Work Flow](../concepts/work-flow.md). El [actor](../concepts/actor.md) **no** es una propiedad permanente de una persona ni una cuenta de sistema.

## Preguntas que orientan

- ¿Quién puede intervenir en el ámbito de trabajo estudiado y qué relación mantiene con él?
- ¿Desde qué posición participa en este contexto, y cuándo podría hacerlo desde otra?
- ¿Qué distinciones entre tipos de [actor](../concepts/actor.md) hace realmente la organización?
- ¿Qué casos observados contradicen nuestra primera clasificación?
- ¿Qué afirmaciones provienen de la organización y cuáles son interpretaciones nuestras?

## Evidencia y límites

Utilizar entrevistas, procedimientos, ejemplos de trabajo real, documentos organizacionales y sistemas existentes **como evidencia**, no como autoridad automática. Separar **observado**, **acordado**, **hipótesis** y **pendiente**.

La distinción **interno / externo** puede ser pertinente, pero es **contextual a la posición desde la que se participa**, no al contrato laboral. Una misma persona podría ser un [actor](../concepts/actor.md) interno en una gestión y externo en otra.

No confundir:

| Concepto | Qué distingue |
|---|---|
| [Participante](../concepts/participant.md) | Persona, colectivo, organización o sistema que interviene |
| Actor | Posición o calidad de participación dentro del contexto |
| [Perfil](../concepts/profile.md) | Función o responsabilidad que puede asumir un [actor](../concepts/actor.md) en un ámbito particular |
| Identidad, cuenta, permiso | Mecanismos técnicos, no definiciones de [actor](../concepts/actor.md) |

## Cómo elaborar el modelo

1. **Delimitar el contexto** de trabajo que se investiga; declarar el alcance sin presuponer la solución de software.
2. **Recopilar [participantes](../concepts/participant.md) y situaciones reales**, buscando posiciones distintas de participación.
3. **Proponer tipos de [actor](../concepts/actor.md)** por las distinciones que explican esas situaciones, no por organigramas, cargos o interfaces.
4. **Contrastar la clasificación** con casos frontera: una persona en dos posiciones, equipos externos operando por delegación, sistemas [participantes](../concepts/participant.md).
5. **Registrar la definición una sola vez** en su documento propietario; enlazar los tipos de [actor](../concepts/actor.md) desde otras superficies.

No crear todavía un inventario exhaustivo de permisos o [perfiles](../concepts/profile.md): pertenecen a preguntas posteriores.

## Resultado examinable

Un conjunto navegable de **tipos de [actores](../concepts/actor.md) contextualizados** con: definición, frontera, ejemplos de participación, procedencia y dudas abiertas. Es suficiente para pasar al siguiente estudio cuando permite identificar quiénes intervienen **sin inventar responsabilidades funcionales**.

**Comprobaciones:** ¿la clasificación depende indebidamente de la situación contractual?, ¿está escrita como si una persona fuera siempre del mismo tipo?, ¿se inventaron permisos?, ¿podemos reconstruir por qué se distinguió cada [actor](../concepts/actor.md)?

## Relación con los pasos siguientes

[Reconocer procesos](02-reconocer-procesos.md) revela dónde aparece la participación de los [actores](../concepts/actor.md). [Identificar perfiles](03-identificar-perfiles.md) precisa qué responsabilidades desempeñan en los [Work Flows](../concepts/work-flow.md). Ambas observaciones pueden obligarnos a revisar la clasificación inicial.

## Evidencia de referencia

[Actores en la documentación de Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/actors/README.md). El ejemplo informa la guía, pero no obliga a copiar su clasificación para otros contextos.
