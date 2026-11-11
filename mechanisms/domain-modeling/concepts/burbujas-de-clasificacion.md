# Burbujas de clasificación — agrupaciones conceptuales candidatas

**Estado:** concepto candidato del Mecanismo de modelado de dominio (Domain Modeling), en exploración durante el paso 6 de [System Realizations](system-realizations.md).

Una **burbuja de clasificación** es una agrupación revisable de conceptos reconocidos durante la sistematización del trabajo. Permite proponer y examinar maneras de organizarlos sin convertir la agrupación, por sí sola, en un módulo, una capa arquitectónica, una frontera de servicio o una unidad de despliegue.

## Burbujas iniciales aportadas por VSlices

Para comenzar a clasificar los conceptos nombrados, VSlices aporta **tres burbujas disponibles por defecto**:

- **[Space](https://github.com/vslices/lang-specification/blob/main/concepts/C-002-space.md):** permite reconocer conceptos y las condiciones de admisibilidad de sus Points, sin asumir por ello que se haya formalizado un Space en una realización.
- **[Feature](https://github.com/vslices/lang-specification/blob/main/concepts/C-020-feature.md):** permite reconocer comportamientos funcionales con intención y contrato de entrada, salida y promesa de resultado, sin reducirlos a endpoints, métodos o mecanismos de activación.
- **[Capability](https://github.com/vslices/lang-specification/blob/main/concepts/C-007-capability.md):** permite reconocer operaciones o familias de operaciones que un comportamiento puede solicitar u ofrecer, independientemente del mecanismo que las realiza.

Estas son **categorías de clasificación iniciales**, no una lista exhaustiva ni una exigencia de que todo concepto entre en una de ellas. Las fichas enlazadas de **Language Specification** articulan estos conceptos para VSIR y conservan la autoridad conceptual de **[VSlices Framework](../../../products/framework/README.md)**. Domain Modeling los emplea para explorar y relacionar conceptos, sin redefinirlos ni confundir las burbujas **Space, Feature y Capability** con las superficies organizacionales **Spaces** y **Work** (véanse [C-021 — Spaces](https://github.com/vslices/lang-specification/blob/main/concepts/C-021-spaces.md) y [C-005 — Work](https://github.com/vslices/lang-specification/blob/main/concepts/C-005-work.md)).

## Burbujas descubiertas durante el estudio

Las personas que modelan pueden añadir otras burbujas cuando el dominio y el propósito del estudio lo justifiquen. Por ejemplo, una burbuja «Tickets» podría relacionar conceptos, funcionalidades y capacidades asociados al trabajo con tickets; otra podría reunir conceptos según la participación de un perfil. Una burbuja «Módulo» puede surgir como hipótesis organizativa **sin quedar validada automáticamente como frontera técnica**.

Una agrupación puede atravesar distintas categorías; no es necesario decidir por adelantado que las burbujas son mutuamente excluyentes o jerárquicas. Las relaciones y límites concretos deben estudiarse en cada caso.

## Propiedades para examinar agrupaciones

- [Coherencia](coherencia.md): examinar qué significado o propósito vuelve razonable la agrupación.
- [Cohesión](cohesion.md): examinar qué relaciones, responsabilidades y razones de cambio justifican tratar conjuntamente esos conceptos.

Se puede volver a nombrar conceptos, reagruparlos, dividir burbujas o proponer otras a medida que aparezca evidencia. El [Acoplamiento](acoplamiento.md) tiene una entrada reservada para el **paso 7**; no se adelanta aquí su examen para dividir la solución.

**Procedencia:** propuesta de clasificación inicial para el paso 6, a partir de la investigación de Serviu Tickets (2026-11-11). No constituye todavía una guía de procedimiento aprobada.
