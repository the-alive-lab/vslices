# VSlices Design — iterative lifecycle

**Owner:** VSlices Design
**Status:** approved conceptual definition (2026-10-09); detailed operational practices may still be candidates.

## Cycle

```text
Understanding
    ↓
Contextualizing
    ↓
Planning
    ↓
Building
    ↓
Validating
    ↺ Understanding
```

The five phases and their conceptual meanings belong to Design, not Method or Planifications. They are not a rigid checklist; relevant uncertainty and evidence determine attention.

## Phases

### Understanding

Develop a justified understanding of the actual problem and work, instead of treating an expressed feature request as sufficient specification. Seek relevant actors, concepts, actions, constraints, consequences, assumptions and uncertainties.

### Contextualizing

Situate that understanding among relevant domain, organizational and technical contexts; make boundaries, responsibilities, dependencies and pressures visible before prematurely fixing a system design.

### Planning

Examine possible responses, compare candidate realizations, responsibilities and constraints, and make the necessary provisional decisions to proceed. Planning does not have to settle technical questions that can responsibly be tested in Building.

### Building

Realize and test the selected response. Implementation and runtime behavior can provide evidence that confirms or challenges prior understanding and decisions.

### Validating

**Contrast the results of an iteration with understanding of the problem, expectations, acceptance criteria, and observed consequences. Incorporate new evidence, identify discrepancies, and respond to feedback received, if any.** Results may confirm, question or change the understanding, decisions and realizations behind the iteration.

Validation is not limited to technical verification. Responding to feedback may mean accepting an observation, explaining a decision, investigating a contradiction, proposing a revision, or explaining why a request is not justified; it **does not imply automatic acceptance**.

New evidence from Validating informs the return to Understanding. Any need to refresh [Method Orientation](../method/orientation.md) may be identified here, but that does not make Orientation a sixth phase.

## Historical evolution (do not rewrite retrospectively)

1. Original: `Understanding -> Contextualizing -> Planning -> Building -> Understanding`.
2. Later discussion: the explicit need for validation led to `Understanding -> Contextualizing -> Planning -> Building -> Validating -> Understanding`.
3. An intermediate Suite model incorporated `Orientation -> ... -> Feedback -> Orientation`, usefully surfacing continuity and feedback but conflating different responsibilities.
4. The approved conceptual correction restores a **five-phase Design iteration** with Validating (which may respond to feedback), with Orientation subsequently defined as a distinct Method responsibility.

The public docs and existing operational protocols may still reflect prior cycles until their projection/application is migrated. Do not mistake those older texts for silently superseding this approved Design definition.

## Relationship with modalities and Method

Design owns modality semantics, including Context-First, Problem-First and Slice-First. Method reasons about selecting or changing them in concrete circumstances, e.g. changing from Context-First to Problem-First because uncertainty, priorities and continuity have changed. Planifications operationalizes the work without owning the five phase meanings.

## Open

- Operational realization and conditions for refreshing Method-owned Orientation.
- Detailed stage contracts, if they are warranted by evidence.
- Migration and validation of existing modality descriptions against product-owned Design sources.
