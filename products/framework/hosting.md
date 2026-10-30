# Hosting — superficie de ensamblaje y publicación de un participante

**Producto propietario:** VSlices Framework.  
**Estado:** **orientación conceptual nueva acordada**, pendiente de precisar contratos y vocabulario técnico.

## Responsabilidad
**Hosting ensambla** las definiciones y realizaciones necesarias para ofrecer las funcionalidades de un servicio o producto en un entorno concreto. Selecciona proveedores, los conecta con las formas de exposición/activación declaradas en Work, configura el runtime y su ciclo de vida, y permite que las Features queden disponibles mediante los mecanismos elegidos.

Work puede asociar una funcionalidad a diversas formas, por ejemplo `Endpoint` y `TimedTask`. Grounding aporta las realizaciones tecnológicas; Hosting decide qué realizaciones se ponen en funcionamiento y cómo se coordinan en el host. Por ejemplo, un Hosting podría publicar Endpoints mediante una API REST o CLI y activar TimedTasks con un scheduler, siempre según contratos explícitos.

## Fronteras
- Hosting **no es sinónimo de EntryPoints**: incluye ensamblaje, configuración y ciclo de vida además de invocación.
- No sustituye a Spaces, no define la semántica de las Features y no absorbe la implementación de las capacidades de Grounding.
- **Hosting no es Composition**: Hosting hace disponible un participante; Composition reúne productos, servicios, recursos y versiones y verifica compatibilidad del conjunto.
- El proyecto `[dominio].Hosting` es candidato de organización física. Esta descripción de responsabilidad no asegura sintaxis o interfaces Framework ya implementadas.

## Preguntas pendientes
Establecer si el núcleo reutilizable de asociar una forma de exposición con un proveedor pertenece por completo a Grounding o requiere un contrato adicional de Hosting. Determinar nombres y contratos para exposiciones múltiples, su configuración, garantías y control del ciclo de vida. No convertir los ejemplos REST/CLI/gRPC/TimedTask en obligaciones universales.
