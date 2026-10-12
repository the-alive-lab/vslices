# Value Orientations — provisional VSlices mechanism model

**Status:** `candidate` — clarified working conceptualization (2026-10-12), not empirically validated.  
**Ownership:** provisional VSlices Suite placement; Method consumes this model for modality selection. Ownership remains reviewable.

## Purpose and scope

**Value Orientations** is the proposed collective name for three **competing emphases that guide the *process* of one standalone group's VSlices iteration**, in response to evidence about organizational needs, available knowledge and operating context. This name better represents a direction of effort than the earlier term **Advancement Paths** (literally, paths of progress/advance).

The historical names `Path of Most Value`, `Path of Most Continuity` and `Path of Least Resistance` remain discoverable as legacy candidate definitions and provenance, but are **not three compulsory routes or process stages**.

| Orientation | Priority during the iteration |
| --- | --- |
| **Most Value** | Deliver business value in the short term. |
| **Most Continuity** | Develop durable business value over the longer term, particularly meaningful continuity between organizational processes and software. |
| **Least Resistance** | Deliver business value with the least justified effort given the actual constraints. |

**Process priority is not equivalent to outcome:** a Least Resistance iteration may yield lasting value without having been governed by Most Continuity. These criteria might influence one another; independence, completeness and exact trade-offs are unproven.

## From evidence to modality decision

```text
Orientation (Method)
    ├── local and general uncertainty: what organization and team know
    ├── needs, problems and opportunities across organizational parts
    ├── organizational, financial, delivery and institutional context
    ├── available experts, sources, capacities, permissions and constraints
    └── previous Validating retrospective / feedback responses, if available
        ↓
interpreted Work Forces (semantic, technical, delivery, resource)
        ↓
relative Value Orientations emphasis (revisable candidate)
        ↓
Method Modality Selection / Switching
        ↓
one standalone Design iteration
        ↓
new evidence / Validating → next Orientation
```

**Uncertainty describes knowledge**, including local vs general understanding of both the organization and the developing team. **Context** also contains pressures (e.g. an economic deadline) which are not themselves knowledge of organizational processes. **Needs** concern desired changes or problems/opportunities. Work Forces offer a possible interpretation of this evidence and help shift the candidate emphasis among orientations. None is a deterministic input-to-score mapping.

Orientation is the recommended Method analysis between Design iterations (and initially), not a covert Context-First. Modality Selection is a **separate judgment** about a viable strategy to advance the actual resolution.

## Candidate affinities — not unconditional mappings

Under strong/extreme conditions an orientation may make one modality especially defensible:

- **Most Value / Problem-First:** an identifiable urgent business problem makes specific problem-directed advancement valuable; this still requires enough evidence to work on the problem responsibly.
- **Most Continuity / Context-First:** sufficient access to organizational process knowledge may support broad work relating processes to software and building lasting traceability. **Knowing one's processes does not mean that the software already preserves their continuity.** Context-First develops that relation rather than merely documenting what the client already knows.
- **Least Resistance / Slice-First:** a time-constrained organization lacking general organizational understanding but possessing reliable *local* knowledge may advance through safe, bounded realizations, growing general understanding incrementally.

**These are situated intuitions, not universal equivalences.** Lack of general knowledge does not automatically imply Slice-First. It may also make Context-First **infeasible when no appropriate experts or other trustworthy broad sources are accessible**. Every candidate must be checked for feasibility, material risk, authority, knowledge dependencies and alternative explanations.

## Change of emphasis

The relative position may change when Orientation or Design reveals new evidence, the business context changes, or previous Validating supplies retrospective artifacts and responses to received feedback. Document what changed **in the interpretation and priorities**, not merely a visual new position. This does not require fixed scores or a forced switch between modalities.

See [Work Forces](../forces/README.md), [Method Orientation](../products/method/orientation.md), [Modality Selection](../products/method/modality-selection.md), [Modality Switching](../products/method/modality-switching.md), and the [triangle playground specification](../playgrounds/value-orientations/README.md).

## Explicit exclusion: composite iterations

This candidate currently models **a single standalone group's iteration only**. It does **not** model parent VSlices iterations coordinating multiple sequential or parallel child groups, potentially each with different orientations. Parent/child aggregation and orchestration remain future exploration.

## Status, history, and open research

This note is a **current working refinement** of previous Path descriptions, not evidence that the three semantic definitions were already identical, nor proof that this explains decisions historically. The prior documents remain as historical entrypoints with explicit pointers to this proposal.

Open: whether these are really three basic orientations; whether Work Forces are the correct interpretation layer; the appropriate ownership/category/name; when high-priority orientations discriminate modalities; whether a triangle is useful without unjustified precision.

[Research Input #23](https://github.com/vslices/research-space/issues/23) and Seyra's study [VS-STU-021](https://github.com/vslices/research-space/blob/research/2026-10-12-vslices-reasoning-reconstruction/lines/vslices/studies/stu-021-reconstruccion-seleccion-modalidad.md) may challenge these claims. Do not rewrite historical decisions or treat this proposal as an approved selection algorithm.
