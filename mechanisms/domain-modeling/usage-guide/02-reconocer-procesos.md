# Paso 2 — Reconocer los procesos semánticos de trabajo

**Estado:** guía candidata, elaborada a partir del modelado organizacional de Serviu (2026-11-10).  
**Pertenece a:** [Guía de uso de Work Semantics](README.md).  
**Definición del mecanismo:** [Domain Modeling](../README.md).

## Propósito

Comprender **qué trabajo reconoce y coordina la organización**, cuáles son los resultados que persigue y **qué acciones semánticas se relacionan** dentro de cada proceso. Este paso parte de los [actores reconocidos](01-reconocer-actores.md), pero permite revisar esa clasificación si aparecen nuevas formas de participación.

## Preguntas que orientan

- ¿Qué servicio, producción o responsabilidad motiva este conjunto de esfuerzos?
- ¿Qué cadena de trabajo lo contiene, y qué parte reconocible de ella estamos estudiando?
- ¿Cuál es el propósito y el resultado del Work Process?
- ¿Qué acciones constituyen Work Flows **con significado propio** para la organización?
- ¿Qué relaciones, condiciones, alternativas o retornos existen entre esas acciones?
- ¿Qué decisiones pertenecen al proceso y cuáles al interior de una acción?

## Evidencia y límites

Contrastar cómo las personas **describen y realizan** el trabajo, procedimientos organizacionales, excepciones y casos observados. Las pantallas, endpoints, transiciones de estado y nombres de Features pueden aportar pistas, **pero no definen por sí mismos** el proceso organizacional.

Conservar la separación entre trabajo **actual**, trabajo **propuesto** y trabajo **deducido**. Si un diagrama de sistema no refleja el comportamiento organizacional, registrar la discrepancia en lugar de ocultarla.

## Cómo elaborar el modelo

1. **Ubicar la cadena relevante (Work Chain)**: qué trabajo conecta y qué límite del problema estudiaremos.
2. **Reconocer el Work Process** por su intención y resultado, no por la cantidad de funciones o pantallas.
3. **Identificar Work Flows candidatos**: nombrar acciones por lo que significan para el trabajo (p. ej., «Registrar solicitud de soporte»), no por verbos CRUD o clases técnicas.
4. **Examinar relaciones entre acciones**: orden necesario, bifurcaciones significativas, retornos, condiciones y consecuencias. No asumir linealidad universal.
5. **Representar el proceso a su nivel**: reflejar las acciones y relaciones suficientes; dejar decisiones operativas internas para el documento de cada Work Flow.
6. **Contrastar con un caso real** y revisar la descomposición cuando la evidencia no coincida.

Jerarquía candidata:

```text
Work Chain
  Work Process
    Work Flow
```

Un **Work Flow** es una acción semántica específica; **no** es el sinónimo de cualquier flecha en el diagrama ni un endpoint. Un Work Process tampoco es una instancia de workflow administrada por un orquestador.

## Representación y ejemplos

El diagrama del **Work Process** pertenece a su documento propietario. Puede ser un grafo simple de acciones con condiciones en los enlaces. No agregar obligatoriamente nodos de decisión si basta una condición en la relación; tampoco prohibirlos cuando expresen una decisión de negocio significativa.

Mantener los nombres del trabajo independientes del lenguaje técnico de la implementación. El detalle de entrada, evaluación y consecuencia de una acción individual se examinará al **profundizar su Work Flow**, no repitiendo el diagrama global.

## Resultado examinable

Un índice de cadenas y procesos, y **un documento propietario por Work Process** con: alcance, propósito, resultado, Work Flows que lo integran, relaciones relevantes, evidencia, nivel de certeza y preguntas abiertas. El diagrama es **una proyección**, no la única fuente del significado.

**Comprobaciones:** ¿se puede explicar el proceso sin hablar de servicios o endpoints?, ¿cada Work Flow representa una acción reconocible?, ¿el diagrama mezcla pasos internos de otras acciones?, ¿las condiciones tienen respaldo?, ¿hay decisiones inventadas solo para completar el gráfico?

## Relación con los pasos siguientes

[Identificar perfiles](03-identificar-perfiles.md) examina quién realiza cada Work Flow y puede hacer visibles responsabilidades o acciones omitidas. Profundizar los Work Flows es un paso posterior aún sin guía especializada.

## Evidencia de referencia

[Work Process «Gestión de solicitud de soporte» en Serviu](https://github.com/atom-dev-serviu/documentation/blob/main/organization/tickets/management-process.md). Su proceso concreto no se reproduce aquí ni se convierte en patrón obligatorio.
