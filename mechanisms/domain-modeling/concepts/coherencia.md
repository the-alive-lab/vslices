# Coherencia — propiedad del modelo

**Estado:** concepto candidato del Mecanismo de modelado de dominio (Domain Modeling), identificado durante la exploración de System Realizations.

**Coherencia** es una **propiedad examinable del modelo** respecto de la compatibilidad de significado, propósito y responsabilidades de los conceptos y sus relaciones.

En el paso 6, permite interrogar si los conceptos que se reúnen en una **burbuja de clasificación** tienen sentido juntos, independientemente de que pertenezcan a categorías distintas (por ejemplo, Space, Feature, Capability, perfil o invariante).

No es una regla de pertenencia automática ni un criterio exclusivamente arquitectónico. Una agrupación coherente es una hipótesis revisable con la comprensión del dominio y la evidencia disponible.

**Relación:** [Cohesión](cohesion.md) es otra propiedad examinable del modelo; ambas pueden ayudar a revisar agrupaciones, sin confundirse entre sí. [Acoplamiento](acoplamiento.md) se reserva para la investigación posterior del paso 7.

**Procedencia:** propuesta elaborada en la exploración del paso 6 con Serviu Tickets (2026-11-11). La [arquitectura de solución de VSlices](../../../products/framework/service-product-nexus.md) ya menciona coherencia, cohesión y acoplamiento como criterios a examinar; este archivo propone su responsabilidad en Domain Modeling, sin atribuirle retroactivamente a esa fuente esta definición.
