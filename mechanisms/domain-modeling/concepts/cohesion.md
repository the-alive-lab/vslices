# Cohesión — propiedad del modelo

**Estado:** concepto candidato del Mecanismo de modelado de dominio (Domain Modeling), identificado durante la exploración de System Realizations.

**Cohesión** es una **propiedad examinable del modelo** respecto de cuánto justifican las relaciones entre conceptos considerarlos conjuntamente, en particular por responsabilidades, comportamientos o razones de cambio compartidas.

En el paso 6, ayuda a interrogar qué conceptos **tienden a cambiar juntos** y si esa evolución compartida tiene una explicación en el dominio. El cambio conjunto es una pregunta de investigación, no una prueba suficiente ni una fórmula de clasificación.

Puede examinarse en las **burbujas de clasificación** sin exigir que agrupen un único tipo de concepto ni que se traduzcan directamente en módulos, capas o servicios. Las agrupaciones se pueden formar y revisar conforme aparece evidencia.

**Relación:** [Coherencia](coherencia.md) examina la compatibilidad de significado y propósito en el modelo. [Acoplamiento](acoplamiento.md) queda reservado para su estudio posterior en el paso 7; no se utiliza aquí para resolver prematuramente la división de la solución.

**Procedencia:** propuesta elaborada en la exploración del paso 6 con Serviu Tickets (2026-11-11). La [arquitectura de solución de VSlices](../../../products/framework/service-product-nexus.md) ya menciona coherencia, cohesión y acoplamiento como criterios a examinar; este archivo propone su responsabilidad en Domain Modeling, sin atribuirle retroactivamente a esa fuente esta definición.
