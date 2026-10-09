# VSlices Design — canonical product-owned definition

**Semantic owner:** VSlices Design.
**Maturity:** approved conceptual core; other details remain candidates.
**Hosting:** this product-owned namespace is canonical within `the-alive-lab/vslices-suite`, the shared source-of-truth repository for the Suite and its products. Design retains conceptual authority within that repository; no standalone Design repository is required.

## Purpose

VSlices Design defines working methodologies, modalities, and reasoning techniques to progressively **understand the client's problem and its context**, **discover and justify requirements**, explore alternatives, and examine realizations. Requested features and proposed solutions are evidence to investigate, not automatically validated requirements. A justified result may be to avoid building software.

Design defines **what a methodology, modality or phase means**. It does not own inter-product coordination merely because another VSlices product uses Design. Method coordinates usage of distinct VSlices product responsibilities; Planifications expresses reusable procedures that invoke them.

## Approved iterative lifecycle

See [Lifecycle](lifecycle.md).

```text
Understanding -> Contextualizing -> Planning -> Building -> Validating
      ^                                               |
      +-----------------------------------------------+
```

Each of these five phases belongs conceptually to **Design**. After Validating, the iteration returns to Understanding, informed by what was learned. This does not mandate equal effort in every phase.

**Validating:** Contrast iteration results with problem understanding, expectations, acceptance criteria and observed consequences. Incorporate evidence, identify discrepancies and **respond to received feedback, when provided**. Its results may confirm, question or revise earlier understanding, decisions or realizations. Answering feedback does not mean automatically accepting requests.

## Modalities

**Design defines** Context-First, Problem-First and Slice-First and their meaning. **Method decides** when to use or switch modalities given uncertainty, priorities and continuity. All three modalities now have bounded canonical definitions: [Context-First](modalities/context-first.md), [Problem-First](modalities/problem-first.md), and [Slice-First](modalities/slice-first.md). Their histories and unresolved questions remain explicit in each source.

## Orientation — unresolved ownership

Orientation is **not a sixth phase** of Design's approved iteration. Establishing enough continuity on entry to work and updating that orientation after validation are recognized needs, but **whether Orientation's definition belongs to Method or Design remains open**. No automatic re-entry phase is authorized by this document.

## Other source boundaries

- **Method:** coordinates the relationship/use of VSlices product responsibilities and context-sensitive modality changes.
- **Docs Standard:** owns documentary structures for preserving knowledge; not the methodologies that generated it.
- **Framework:** owns its executable representations/realizations; not Design's problem-understanding method.
- **Planifications:** coordinates procedural application during runs; not Design semantics.
- **vslices/docs:** public projection, not the origin of these meanings.

## Traceability

- [Lifecycle definition and historical transition](lifecycle.md).
- [Current Suite cross-product responsibilities](../README.md).
- [Decision and unresolved questions](../design-method-boundary-review.md).
- [Public Design projection (historical/current until updated)](https://github.com/vslices/docs/blob/main/es/products/design/index.md).

Future migrations must preserve provenance and distinguish approved meanings from unfinished techniques.
