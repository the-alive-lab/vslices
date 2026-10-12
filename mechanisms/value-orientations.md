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

## Evidence interpretation and responsibility

**Orientation Factors** is the revised working name for Work Forces, describing interpreted Semantic, Technical, Delivery and Resource evidence. A document interpretation may have no current material effect. New evidence can lead to reclassification or nuance and corresponding justified impact, reconsidering factor interpretations before the triangle's recommendation. The candidate [documentary reinterpretation mechanism](documentary-reinterpretation.md) explores this propagation through explicit front-matter relations, not tags. The triangle does not itself own documentary traversal.

## From evidence to modality decision

```text
Orientation (Method)
    ├── local and general uncertainty: what organization and team know
    ├── needs, problems and opportunities across organizational parts
    ├── organizational, financial, delivery and institutional context
    ├── available experts, sources, capacities, permissions and constraints
    └── previous Validating retrospective / feedback responses, if available
        ↓
interpreted Orientation Factors (semantic, technical, delivery, resource)
        ↓
relative Value Orientations emphasis (revisable candidate)
        ↓
Method Modality Selection / Switching
        ↓
one standalone Design iteration
        ↓
new evidence / Validating → next Orientation
```

**Uncertainty describes knowledge**, including local vs general understanding of both the organization and the developing team. **Context** also contains pressures (e.g. an economic deadline) which are not themselves knowledge of organizational processes. **Needs** concern desired changes or problems/opportunities. Orientation Factors offer a possible interpretation of this evidence and help shift the candidate emphasis among orientations. None is a deterministic input-to-score mapping.

Orientation is the recommended Method analysis between Design iterations (and initially), not a covert Context-First. Modality Selection is a **separate judgment** about a viable strategy to advance the actual resolution.

## Candidate affinities — not unconditional mappings

Under strong/extreme conditions an orientation may make one modality especially defensible:

- **Most Value / Problem-First:** an identifiable urgent business problem makes specific problem-directed advancement valuable; this still requires enough evidence to work on the problem responsibly.
- **Most Continuity / Context-First:** sufficient access to organizational process knowledge may support broad work relating processes to software and building lasting traceability. **Knowing one's processes does not mean that the software already preserves their continuity.** Context-First develops that relation rather than merely documenting what the client already knows.
- **Least Resistance / Slice-First:** a time-constrained organization lacking general organizational understanding but possessing reliable *local* knowledge may advance through safe, bounded realizations, growing general understanding incrementally.

**These are situated intuitions, not universal equivalences.** Lack of general knowledge does not automatically imply Slice-First. It may also make Context-First **infeasible when no appropriate experts or other trustworthy broad sources are accessible**. Every candidate must be checked for feasibility, material risk, authority, knowledge dependencies and alternative explanations.

## Position, recommendation, and evidence quantity (candidate semantics)

The triangle is a **semantic response space** with three corners: **Most Value → Problem-First**, **Most Continuity → Context-First**, **Least Resistance → Slice-First**. Proximity to a corner expresses **stronger recommendation affinity** for its associated Design modality. An edge position means the two corresponding responses remain defensible; the center permits all three. Distance from other corners exposes **relative trade-offs and risk questions**, not a measured probability or risk magnitude.

**Position and evidence quantity are separate dimensions.** A midpoint with little evidence may reflect underdetermination, **not** a demonstrated 50/50 choice. The same midpoint after substantially more relevant evidence may express a genuine balance between defensible responses. For an initial playground, evidence quantity may be displayed as the **count of traceable evidence items considered**, not a calibrated statistical confidence score. Counts alone do not prove quality, independence, coverage or validity: duplicate, irrelevant or contradictory documents must remain visible rather than artificially increasing certainty. A reliable semantic confidence model remains future research.

Feasibility is evaluated **inside the Orientation Factors interpretation**, notably the availability and distribution of local/general knowledge and uncertainty of the organization and team. A recommendation should therefore be derived from **interpreted feasible responses**, not from an unconstrained triangle position followed by a separate invented feasibility gate. Low general knowledge without accessible organizational experts can render Context-First infeasible; adequate local knowledge may make a bounded Slice-First feasible, but neither conclusion is automatic.

## Interpreted movement, not automatic evidence displacement

A new document does not directly push the point. Actors (or a supported LLM hypothesis subject to review) **interpret evidence as Orientation Factors**, including the local/general uncertainty that influences what responses can responsibly be attempted. That interpretation justifies retaining or changing the recommended position. Different legitimate interpretations can produce different candidate positions. The rationale and its source relationship can be preserved through **Docs Standard**; the triangle does not own an additional mandatory documentation or history format.

The core proposed reasoning is:

```text
evidence and context → interpretation into Orientation Factors
                     → feasible response affinities
                     → Value Orientations position + evidence quantity
                     → Method modality recommendation
```

This is a proposed **semantic interpretation model**, not an arbitrary scoring algorithm, fixed geometric risk calculation or automatically validated LLM judgment.

## Change of emphasis

The relative position may change when Orientation or Design reveals new evidence, the business context changes, or previous Validating supplies retrospective artifacts and responses to received feedback. Document what changed **in the interpretation and priorities**, not merely a visual new position. This does not require fixed scores or a forced switch between modalities.

See [Orientation Factors](../forces/README.md), [Method Orientation](../products/method/orientation.md), [Modality Selection](../products/method/modality-selection.md), [Modality Switching](../products/method/modality-switching.md), and the [triangle playground specification](../playgrounds/value-orientations/README.md).

## Explicit exclusion: composite iterations

This candidate currently models **a single standalone group's iteration only**. It does **not** model parent VSlices iterations coordinating multiple sequential or parallel child groups, potentially each with different orientations. Parent/child aggregation and orchestration remain future exploration.

## Status, history, and open research

This note is a **current working refinement** of previous Path descriptions, not evidence that the three semantic definitions were already identical, nor proof that this explains decisions historically. The prior documents remain as historical entrypoints with explicit pointers to this proposal.

Open: whether these are really three basic orientations; whether Orientation Factors are the correct interpretation layer; the appropriate ownership/category/name; when high-priority orientations discriminate modalities; whether a triangle is useful without unjustified precision.

[Research Input #23](https://github.com/vslices/research-space/issues/23) and Seyra's study [VS-STU-021](https://github.com/vslices/research-space/blob/research/2026-10-12-vslices-reasoning-reconstruction/lines/vslices/studies/stu-021-reconstruccion-seleccion-modalidad.md) may challenge these claims. Do not rewrite historical decisions or treat this proposal as an approved selection algorithm.
