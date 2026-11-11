# Continuidad entre Work Semantics y System Realizations

**Estado:** relaciones y movimientos candidatos; no son transformaciones obligatorias.  
**Mecanismo:** [Domain Modeling](../README.md).

El paso desde [Work Semantics](work-semantics.md) hacia [System Realizations](system-realizations.md) **descubre y expresa** conceptos, comportamientos, restricciones y capacidades. No representa una traducción directa de organigramas o diagramas de proceso a clases de software.

## Correspondencia candidata

| Comprensión / elaboración | Work Semantics | System Realizations |
|---|---|---|
| Cadena de trabajo | [Work Chain](work-chain.md) | — |
| Proceso organizacional | [Work Process](work-process.md) | — |
| Acción organizacional y posible sistematización | [Work Flow](work-flow.md) | [System Process](system-process.md) |
| Acción funcional | — | [System Action](system-action.md) (nombre candidato) |
| Operación concreta | — | [System Step](system-step.md) |

La fila compartida expresa una **relación posible**, no identidad, equivalencia ni correspondencia uno a uno. Una acción organizacional puede requerir capacidades múltiples o ninguna realización sistematizada.

## Movimientos de elaboración

Los movimientos expresan preguntas de comprensión y revisión:

- **Concretizar trabajo:** `Work Chain → Work Process → Work Flow`. ¿Qué acciones hacen reconocible la cadena y sus procesos?
- **Abstraer trabajo:** `Work Flow → Work Process → Work Chain`. ¿Qué propósito y contexto explican estas acciones?
- **Sistematizar:** `Work Flow → System Process`. ¿Qué coordinación de capacidades podría realizar el trabajo?
- **Descubrir y expresar:** ¿qué conceptos, restricciones, **Spaces**, **Points**, **Features** y **Capabilities** se justifican en la elaboración de la realización? Véase [Framework](../../../products/framework/README.md) para sus definiciones.
- **Descomponer la realización:** `System Process → System Action → System Step`. ¿Qué responsabilidades y operaciones distinguimos?
- **Reexaminar el trabajo:** ¿qué observaciones de la realización contradicen o precisan nuestras hipótesis de Work Semantics?

No existen transformaciones automáticas afirmadas por esta definición.

## Caso de referencia: solicitud de pago DS 49

**Comprensión organizacional:**

```text
Work Chain: Servicio de financiamiento DS 49
  Work Process: Creación de solicitudes DS 49
    Work Flow: Crear solicitud de pago DS 49
```

**Realización candidata:**

```text
System Process: Atender «Crear solicitud de pago DS 49»
  System Action: Crear solicitud de pago
    System Step: Validar solicitud
    System Step: Persistir cambios
  System Action: Notificar solicitante
  System Action: Notificar revisor
  System Action: Registrar auditoría
```

Esta descomposición no decide sincronía, orden de confirmación, atomicidad, idempotencia, propiedad de datos, frontera de servicios o mecanismos de despliegue.

## Arquitectura y límites

Como caso de referencia, un Producto/BFF puede coordinar un System Process y los Servicios pueden proveer capacidades, mientras Composition integra participantes; **no** es una asignación universal. Véase [Servicio, Producto y Composition](../../../products/framework/service-product-nexus.md).

Un [System Process](system-process.md) no es automáticamente una instancia persistida de proceso gestionada por un orquestador; la definición, estados, reglas, transiciones e historia de esas instancias conservan su propia investigación pendiente.

Los diagramas, carriles y artefactos documentales representan el conocimiento desde una decisión de visualización, sin definir su semántica ni transferir la autoridad sobre ella.
