# Work — superficie de funcionalidades y capacidades requeridas

**Producto propietario:** VSlices Framework.  
**Estado:** responsabilidad organizacional acordada; vocabulario de exposición y contratos específicos aún en investigación.

## Responsabilidad
**Work** organiza las funcionalidades y **las capacidades requeridas por ellas**, incluyendo capacidades de **acceso** y de **exposición o activación**. Una Feature identifica comportamiento, intención y promesa de resultado; no queda reducida a una ruta HTTP, tarea de scheduler ni método de una clase.

La funcionalidad puede asociarse a **más de una forma de exposición o activación** (nombre de esa categoría pendiente). Ejemplos de formas candidatas son `Endpoint` y `TimedTask`. Una sola Feature podría ofrecerse por varios mecanismos sin duplicar su significado.

## Fronteras
- Work define **qué funcionalidad y qué capacidades necesita**, no obliga a implementar el mecanismo ni a elegir tecnología.
- No identificar Work con Application de DDD, procesos HTTP ni con Hosting.
- No inferir que secuencia implica transacción, ni que declarar una capacidad demuestra que exista una realización válida.
- Grounding proporciona mecanismos para realizar las capacidades; Hosting reúne y activa las realizaciones necesarias en un escenario.

## Preguntas pendientes
Nombre y contrato de la categoría que agrupa `Endpoint` y `TimedTask`; cómo expresar multiplicidad de exposiciones; qué garantías corresponden a cada realización; contratos de `Flow`, `WorkFlow`, `WorkProcess` y `WorkStep`. Véase [Work en Language Specification](https://github.com/vslices/lang-specification/blob/main/concepts/C-005-work.md) como articulación existente, sin cerrar estas cuestiones.
