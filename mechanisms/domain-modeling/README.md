# Domain Modeling — modelado de dominio

**Estado:** mecanismo candidato (revisión conceptual del 2026-11-10).  
**Responsabilidad conceptual:** VSlices Suite; los conceptos técnicos utilizados conservan sus autoridades específicas.  
**Procedencia:** evolución de `Action Flow → Work Modeling → Domain Modeling`, a partir de la discusión y el modelado de procesos organizacionales de Serviu. La trayectoria permanece reconstruible en Git y en [Action Flow](../action-flow.md), [Work Modeling](../work-modeling.md) y la versión histórica de este archivo.

## Definición

**Domain Modeling** es la práctica de **comprender y representar un dominio** partiendo de cómo la organización entiende, estructura y coordina su trabajo, para luego descubrir y desarrollar realizaciones sistematizadas que conserven su significado.

VSlices comparte la noción de *domain* asociada a Eric Evans y DDD, **no** una obligación de adoptar su metodología de modelado o su taxonomía de construcciones.

El modelado es **progresivo y revisable**: comprender el trabajo orienta la sistematización; los conceptos, comportamientos y capacidades se descubren durante la elaboración de realizaciones de sistema; la evidencia obtenida puede exigir revisar la comprensión original. Esto no implica una traducción automática entre niveles ni una secuencia rígida.

## Recorrido y revisión

La [guía de uso](usage-guide/README.md) presenta un **orden natural para investigar el dominio**, no fases irreversibles. Los hallazgos posteriores pueden motivar el retorno a un paso anterior para revisar únicamente el conocimiento afectado, siempre de manera coherente con la pregunta y el objetivo general de la investigación. Una revisión material distingue la comprensión previa, la evidencia que la cuestiona y la comprensión revisada; no obliga a reiniciar el recorrido ni a alterar la responsabilidad conceptual de cada paso.

## Objetivo

Preservar la continuidad semántica entre la comprensión del trabajo y las realizaciones estudiadas, sin confundir significado organizacional, construcción conceptual, responsabilidad técnica y decisiones de implementación.

## Documentación

- [Conceptos](concepts/README.md): definiciones propietarias de los conceptos del mecanismo, sus relaciones y límites.
- [Guía de uso](usage-guide/README.md): recorrido inicial de modelado de Work Semantics.
  - [Paso 1 — Reconocer actores](usage-guide/01-reconocer-actores.md).
  - [Paso 2 — Reconocer procesos semánticos de trabajo](usage-guide/02-reconocer-procesos.md).
  - [Paso 3 — Reconocer perfiles organizacionales](usage-guide/03-identificar-perfiles.md).
  - [Paso 4 — Relacionar perfiles con Work Flows](usage-guide/04-relacionar-perfiles-con-work-flows.md).

Las definiciones particulares pertenecen a **concepts/**; este README expresa únicamente el mecanismo, su propósito y las rutas de consulta. Los contratos de Spaces, Features y otras construcciones permanecen bajo [VSlices Framework](../../products/framework/README.md).
