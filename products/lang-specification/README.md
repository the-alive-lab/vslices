# VSlices Language Specification

**Responsabilidad conceptual de producto:** VSlices Language Specification (antes **Intermediate Representation / VSIR**).  
**Estado:** evolución del lenguaje en investigación y especificación; los contratos previos de VSIR 0.1 conservan su vigencia **para los artefactos que declaran esa versión**, sin predeterminar la nueva generación.

## Propósito y autoridad

Language Specification define el lenguaje con el que se pueden **expresar, conservar, interpretar y examinar afirmaciones semánticas sobre software**, y establece sus formas de declaración, relaciones, versionado y condiciones de conformidad. No equivale a Framework, Tooling, Ruleset ni a un lenguaje destino.

- **Esta superficie canónica de Suite** define identidad, propósito y fronteras del producto.
- **[vslices/lang-specification](https://github.com/vslices/lang-specification)** es la superficie especializada donde se revisan conceptos para el lenguaje, se desarrollan especificaciones y se conservan los contratos versionados.
- **Framework** conserva responsabilidad conceptual sobre su semántica de software y sus realizaciones; una articulación de Framework para el lenguaje no se apropia de su definición.
- **Tooling** implementa authoring, validación, interpretación y lowering compatibles con contratos explícitos.
- **Ruleset** aporta conocimiento determinista de realización hacia un target sin inventar semántica ausente.

La distinción entre **concepto**, **declaración del lenguaje**, **regla de conformidad**, **implementación de un parser/lowerer** y **evidencia de ejecución** debe preservarse.

## Estado de la nueva generación

La exploración de la siguiente generación de VSIR se centra inicialmente en expresar conocimiento semántico que pueda orientar una transpilación hacia lenguajes existentes. No es una gramática ni un transpilador completo ya aprobados.

Puntos de entrada del repositorio especializado:

- [README y orientación de revisión](https://github.com/vslices/lang-specification/blob/main/README.md)
- [Conceptos revisados](https://github.com/vslices/lang-specification/blob/main/concepts/README.md)
- [Cola y estado de aprobación](https://github.com/vslices/lang-specification/blob/main/review/queue.json)
- [Cierre de revisión conceptual del 2026-10-24](https://github.com/vslices/lang-specification/blob/main/review/closure-2026-10-24.md)
- [Especificaciones/candidatos de Space](https://github.com/vslices/lang-specification/tree/main/specifications/space)

En ese contexto, [Spaces](https://github.com/vslices/lang-specification/blob/main/concepts/C-021-spaces.md), [Work](https://github.com/vslices/lang-specification/blob/main/concepts/C-005-work.md), [Grounding](https://github.com/vslices/lang-specification/blob/main/concepts/C-006-grounding.md) y [Feature](https://github.com/vslices/lang-specification/blob/main/concepts/C-020-feature.md) han recibido articulaciones conceptuales aprobadas para el lenguaje, **sin reemplazar automáticamente las fuentes semánticas propias de Framework**, ni convertirlas en una estructura física obligatoria.

## Versión anterior y continuidad

El repositorio especializado preserva:

- [SPECIFICATION.md](https://github.com/vslices/lang-specification/blob/main/SPECIFICATION.md)
- [SPECIFICATION-REFINE-INTRINSIC.md](https://github.com/vslices/lang-specification/blob/main/SPECIFICATION-REFINE-INTRINSIC.md)
- [SPECIFICATION-CONDITION-EXPRESSIONS.md](https://github.com/vslices/lang-specification/blob/main/SPECIFICATION-CONDITION-EXPRESSIONS.md)
- [AUTHORING-LOWERING-PARITY.md](https://github.com/vslices/lang-specification/blob/main/AUTHORING-LOWERING-PARITY.md)

Son **contratos y evidencias de la generación anterior**, no prescripciones automáticas para la nueva. Por ejemplo, `kind: domain-type` es vocabulario de VSIR 0.1, mientras Framework ha revisado el significado de *Domain Type*. No reinterpretar silenciosamente un artefacto existente para hacer desaparecer esta tensión histórica.

Distinguir en cada revisión: admisibilidad de un estado parcial de autoría, conformidad respecto de la versión declarada y posibilidad efectiva de realización en un target.

## Relaciones y límites

- No resolver conflictos conceptuales escogiendo simplemente el repositorio donde apareció el término.
- No confundir la aprobación de un concepto con sintaxis admitida, cobertura de Tooling o garantías demostradas.
- No fijar monadas, C#, HTTP, persistencia o un runtime concreto como obligaciones universales de VSIR.
- No declarar que Spaces/Work/Grounding corresponden a Domain/Application/Infrastructure.
- No introducir compatibilidad con versiones anteriores por inercia: una decisión de migración exige examen explícito.

**Semantic Determination** es una [nota candidata localizada en la fuente canónica de Suite](../../mechanisms/semantic-determination-candidate.md); su pertenencia conceptual entre VSlices y PResolver sigue abierta. La [ruta previa en Language Specification](https://github.com/vslices/lang-specification/blob/main/concepts/semantic-determination-candidate.md) conserva un enlace de continuidad.

## Navegación histórica

La instrucción de redirección de la antigua denominación **Intermediate Representation** vive únicamente en [products/README.md](../README.md). No se mantiene un archivo de redirección en la antigua ruta. Los contratos versionados históricos permanecen en el repositorio especializado.
