# Context-First — VSlices Design modality

**Owner:** VSlices Design  
**Status:** canonical migration of the existing modality definition, aligned with the approved five-phase Design lifecycle (2026-10-09). Historical examples are evidence, not universal obligations.

## Definition

**Context-First** is the Design modality that **prioritizes understanding the relevant domain and surrounding business/organizational/system context before committing to specific solutions or software structures**.

It is justified when material contextual uncertainty makes design decisions fragile: the actual work, actors, vocabulary, responsibilities, boundaries, dependencies, or adjacent consequences are insufficiently understood.

Context-First does **not** presuppose a preferred architecture, feature list, API, database model, screen or even that building software is the right outcome. It seeks enough understanding to discover and justify what problem or improvement merits a response.

Its central distinction is **priority of attention**, not a mandatory process, larger documentation inventory, or an infinite discovery effort.

## Emphasis within the approved Design iteration

| Design phase | Context-First emphasis |
| --- | --- |
| **Understanding** | Strong: investigate actual work, actors, concepts, language, assumptions and uncertainties. |
| **Contextualizing** | Strong: relate discoveries into a sufficiently reliable view of the present situation, boundaries, responsibilities, dependencies and adjacent work. |
| **Planning** | Guided by contextual evidence: identify and compare justified improvements, scope and consequences; no requirement to plan everything in advance. |
| **Building** | Realize or experiment with the chosen response while preserving traceability to the understanding; new evidence may contradict it. |
| **Validating** | Contrast observed results against understanding, expectations, acceptance criteria and consequences; **respond to feedback if provided** and identify what changes for the next iteration. |

Context-First uses the **same five phases** as the other Design modalities. It does not add its own phases or redefine Validating. Its difference is the emphasis placed on contextual understanding, especially early in the work.

## Where Context-First helps

Evidence may favor Context-First when:

- work spans poorly understood areas, roles or organizational boundaries;
- current processes are manual, fragmented, legacy-dependent, or tacit;
- participants hold incompatible understandings of the same work;
- decisions affect adjacent workflows, actors or systems;
- incorrect assumptions would create substantial rework or harm;
- the team is entering an unfamiliar domain and cannot yet justify its proposed solution.

These are **indicators**, not a mandatory checklist or a selection algorithm.

## Adequacy and limits

The goal is **sufficient relevant context to support responsible next decisions**, not complete domain knowledge. Progress is visible when uncertainties important to the next decision shrink, responsibilities and affected work become clearer, or candidate problems/improvements can be justified.

Risks include excessive discovery, delayed feedback, unnecessary artifacts, interpreting documentation volume as understanding, and analyzing the organization beyond the scope that can matter.

If further contextual inquiry is unlikely to change a material decision, continuing it needs new justification. Conversely, missing material context may be rediscovered after Building or Validating.

## Responsibility boundary

- **Design** owns this modality's meaning, its focus, strengths, risks, and how it affects attention across Design phases.
- **Method** decides whether to use, continue or switch this modality given actual uncertainty, priorities, consequences and continuity. A possible shift is Context-First to Problem-First once a sufficiently grounded specific problem becomes the dominant concern, but the transition is **not automatic**.
- **Planifications** may coordinate a concrete run's use of the modality without defining or prescribing its semantics.
- **Docs Standard** provides documentary structures if preservation is useful; Context-First itself does not require a fixed document set.

## Provenance and migration decisions

The source of this migration is the current public/historical Design material:

- [Context-First overview](https://github.com/vslices/docs/blob/main/es/products/design/modalities/context-first/index.md)
- [Context-First iteration emphasis and examples](https://github.com/vslices/docs/blob/main/es/products/design/modalities/context-first/iteration-flow.md)
- [Risks and relation to other modalities](https://github.com/vslices/docs/blob/main/es/products/design/modalities/context-first/risks-and-relations.md)
- [Method modality switching](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-switching.md)
- [Anamnesis retrospective recognition](https://github.com/vslices/docs/blob/main/es/decisions/anamnesis-concept-study/0001-reconocer-context-first-retrospectivamente.md)

### What was retained

- Context over premature technological solution.
- Higher Understanding and Contextualizing emphasis.
- Knowledge of current work before final target decisions.
- Explicit stopping pressure; do not model everything.
- Tradeoffs and the possibility of changing modality.
- Context-to-decision-to-realization continuity.

### What was adapted rather than silently copied

The older four-phase exposition treated implementation, validation, delivery and feedback together inside **Building**. Under the **approved** [five-phase Design lifecycle](../lifecycle.md), **Validating is a distinct fifth phase**, including response to feedback **when feedback exists**. This document preserves that historical change instead of reproducing the former cycle as current.

The older public material occasionally phrases “when to use” and modality transitions inside Design. **The meaning and indicators belong to Design**, while **the concrete selection or switch decision belongs to Method** under the clarified product boundary.

The Anamnesis example was identified **retrospectively** as Context-First. It is not evidence that Method had knowingly selected that modality from the beginning.

### Not yet promoted

- An exhaustive elicitation procedure for client problems or requirements.
- A universal set of documents or interviews.
- Numeric context sufficiency or switching thresholds.
- Definition of Problem-First or Slice-First (each needs its own bounded migration).
- Ownership of Orientation.
