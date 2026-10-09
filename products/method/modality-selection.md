# Modality Selection — VSlices Method

**Owner:** VSlices Method  
**Status:** canonical migration of an existing Method pattern (2026-10-09); not a newly invented decision mechanism.

## Purpose

**Modality Selection** determines which VSlices Design modality should guide the present work by examining **the uncertainty that most threatens the next responsible decision and the continuity that work must preserve**.

It does not select an intrinsically best modality, prescribe a universal sequence, or make a modality the permanent identity of an iteration.

> Choose the smallest useful modality emphasis that makes the next responsible decision safer.

Design defines the meanings of Context-First, Problem-First and Slice-First. **Method owns the contextual decision to select one**; the concrete run and its state may be coordinated through Planifications.

## Selection criteria

First determine what is insufficiently known and why that uncertainty matters to the next consequential decision. Then consider:

| Dominant concern | Candidate Design modality | Reason for selection |
| --- | --- | --- |
| The surrounding domain and actual work cannot yet be explained reliably. | **Context-First** | Wider contextual understanding is needed before responsibly narrowing the problem or committing to a solution. |
| A problem or opportunity is visible, but its causes, limits, impact or expected improvement are unclear. | **Problem-First** | Investigating the problem reduces the risk of treating symptoms or optimizing locally. |
| The problem and surrounding context are sufficiently understood, and a small reversible realization can produce more useful evidence than further analysis. | **Slice-First** | Real-world feedback from a bounded slice can make the next decision safer. |

These are indicative relationships, **not exhaustive conditions, a scoring model, or an automatic routing algorithm**. Method should account for actual priorities, consequences, material risks and continuity rather than matching isolated keywords.

## Typical evidence and risks

### When Context-First is useful

Indicators include unfamiliar or tacit domains, manual work, disagreeing actor descriptions, ambiguous vocabulary, unclear workflow limits, or not knowing which problem is material. It guards against realizing software for a misunderstood reality.

Its risk is **analysis without movement**. Further contextual work needs justification once sufficient context supports a responsible next decision.

See [Design's canonical Context-First definition](../design/modalities/context-first.md).

### When Problem-First is useful

Indicators include repeated user pain, a workflow bottleneck, a feature that does not support actual work, visible impact with unknown causes, or premature solution proposals. It guards against solving symptoms.

Its risk is **isolating a problem from its necessary context**. This document does not yet establish a complete canonical definition of Problem-First; that migration remains with Design.

### When Slice-First is useful

Indicators include enough context to act, bounded/reversible risk, material implementation uncertainty, need for feedback from use, or a small slice able to test an assumption. It guards against indefinitely designing without learning from reality.

Its risk is **implementation without enough understanding**. This document does not yet establish a complete canonical definition of Slice-First; that migration remains with Design.

## Selection is revisable

Selection remains sensitive to new evidence. When the dominant uncertainty changes, Method may decide a different modality is justified. The complete **Modality Switching** pattern exists historically in the public Method projection and should be migrated separately rather than redescribed here.

A modality change need not imply failure or restart of the iteration; it can reflect successful learning.

## Boundaries

- **Design** defines the phases, modalities, their emphasis and their meaning.
- **Method** reasons about the modality appropriate to current uncertainty, priorities and continuity; it does not redefine the modalities.
- **Planifications** can operationalize a selected modality in a reusable or concrete procedure without gaining its semantic authority.
- **Docs Standard** may preserve the reason for selection where needed, without requiring an artifact for each choice.

## Provenance and migration decisions

Primary historical source: [VSlices Method — Selección de modalidad](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-selection.md).

Related history:
- [VSlices Method — Cambio de modalidad](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-switching.md)
- [VSlices Method — Guías de contexto](https://github.com/vslices/docs/blob/main/es/products/method/context-guides/index.md)
- [VSlices Design — Context-First](../design/modalities/context-first.md)

Preserved from the existing pattern: focus on dominant uncertainty, next responsible decision, Context-/Problem-/Slice-First applicability, the characteristic risks of each, minimum useful emphasis, and the need to reevaluate selection as learning changes.

Clarified rather than silently moved: the historical Method text provides examples describing the modalities, but their **definition** is Design-owned; examples here illustrate Method's selection decision. No claim is made that all three modalities' full Design semantics have already been migrated.

Not introduced: numerical uncertainty thresholds, compulsory assessment paperwork, a fixed transition ladder, automatic selection, or Orientation ownership. Concrete switching remains a separate existing Method concept.
