# Grounding — superficie de mecanismos de realización

**Producto propietario:** VSlices Framework.  
**Estado:** responsabilidad organizacional acordada; alcance exacto de proveedores de exposición sujeto a revisión.

## Responsabilidad
**Grounding proporciona mecanismos concretos para realizar las capacidades definidas o requeridas por Work**, incluidas capacidades de acceso y, cuando el contrato lo determine, de exposición o activación. Las realizaciones se examinan respecto de sus condiciones de entorno y **Guarantees**; ofrecer un mecanismo no demuestra que satisfaga automáticamente todas las garantías.

Por ejemplo, distintos proveedores podrían realizar una capacidad de publicación de Endpoint mediante REST, CLI o eventualmente gRPC, o una capacidad de activación periódica mediante una tecnología de scheduling. **Son ejemplos exploratorios**, no proveedores implementados o aprobados.

## Fronteras
- Grounding no redefine el comportamiento de una Feature ni la admisibilidad de sus Points.
- Grounding realiza mecanismos; **Hosting selecciona, ensambla, configura y pone en funcionamiento** las realizaciones que un escenario requiere.
- No equivaler Grounding a Infrastructure de DDD, EF Core o persistencia; una Feature puramente funcional puede no necesitar mecanismos externos.
- No confundir presencia de un provider con evidencia de cumplimiento de garantías.

## Preguntas pendientes
Precisar el contrato común para realizar formas como `Endpoint` o `TimedTask`, y el punto exacto donde termina el mecanismo de Grounding y comienza la responsabilidad de Hosting. Véase [Grounding en Language Specification](https://github.com/vslices/lang-specification/blob/main/concepts/C-006-grounding.md) como articulación disponible.
