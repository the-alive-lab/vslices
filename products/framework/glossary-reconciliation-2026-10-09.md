# Framework — conciliación del glosario público (2026-10-09)

**Autoridad conceptual:** VSlices Framework. **Estado:** revisión conceptual; las relaciones detalladas entre algunos conceptos continúan abiertas.

## Propósito y procedencia

VSlices Framework permite expresar o condensar intención de software para sustentar realizaciones, transformaciones, derivaciones, validación, pruebas y reutilización. La [realización .NET](https://github.com/vslices/framework) no agota el significado del producto. El [glosario público](https://github.com/vslices/docs/blob/main/es/products/framework/glossary.md) es evidencia histórica y didáctica, no un inventario automáticamente normativo.

## Conceptos reconocidos

- **Flow:** concepto vigente. Su ausencia o eliminación en `master` no equivale a abandono; las ramas `fix/restore-feature-flow-boundary` y `experiment/flow-algebra-runtime` exploran realizaciones. No congelar una firma genérica como definición universal.
- **Feature:** concepto reutilizable para definir **WorkFlows en Services** y **WorkFlows o WorkProcesses en Products**. No reducirlo al modelo particular de Feature-as-Free actualmente visible en `master`.
- **WorkStep:** concepto pertinente para la unidad de trabajo; el glosario público dice Step y Pipeline, pero eso no demuestra que ambos sean primitivas independientes actuales.
- **Space e invariantes:** `Domain Type` es una categoría histórica retirada. Permanecen reglas de Space, pero el nombre formal vigente `Invariant` requiere comprobación.
- **Result / Error as Value:** continúan relevantes para representar resultados y fallos esperados explícitamente sin convertir excepciones en control ordinario.
- **Trait, Effect y composición funcional:** principalmente recursos de realización; no deben imponerse como significado universal de Framework.
- **Integrator, Adapter, Provider y Port:** vocabulario histórico pendiente de reconciliación con Grounding e invocación.

## Capability

Una **Capability** representa una operación o familia de operaciones que un comportamiento puede solicitar o requerir, independientemente del mecanismo específico que la realiza.

Expresa **qué puede hacerse**, pero no implica por sí sola propiedades adicionales sobre sus efectos o ejecución.

## Guarantee

Una **Guarantee** representa una propiedad o restricción semántica que una realización admisible debe satisfacer, bajo un alcance determinado.

Expresa **qué debe mantenerse verdadero**, independientemente del mecanismo seleccionado. Por ejemplo, atomicidad, durabilidad, aislamiento, tracking, ordenamiento o entrega necesitan definiciones y evidencias propias: no se deducen automáticamente de una Capability ni de una tecnología.

Distinguir **requerimiento**, **realización** y **evidencia**: declarar una garantía no demuestra que se cumpla. La investigación existente contempla `Proven`, `Discharged`, `Unresolved` y `Contradicted` como estados exploratorios. **Unresolved no equivale a Contradicted**.

## Límites y cuestiones abiertas

La implementación .NET explora actualmente Space, Work y Grounding. Estas responsabilidades no necesariamente constituyen una ontología cerrada del Framework.

Quedan por precisar las relaciones y contratos entre Flow, WorkFlow, WorkProcess, WorkStep y Feature, el nombre vigente de las reglas de Space y los límites de los conceptos de integración.

## Referencias

- [Docs públicos: Framework](https://github.com/vslices/docs/tree/main/es/products/framework)
- [Framework: arquitectura](https://github.com/vslices/framework/blob/master/docs/architecture.md)
- [Framework: Capability / Guarantee](https://github.com/vslices/framework/blob/master/docs/notes/capabilities-and-guarantees.md)
- Ramas experimentales de `vslices/framework` y correcciones conceptuales de esta revisión.

La fuente de verdad conceptual vive en VSlices; los repositorios oficiales especializados pueden extenderla y profundizarla sin convertirse en autoridades semánticas competidoras.
