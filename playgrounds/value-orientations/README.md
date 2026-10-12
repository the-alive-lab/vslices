# Value Orientations Playground — candidate specification

**Status:** exploratory proposal, unimplemented; **not** a validated formal model or normative modality selector.  
**Scope:** one **standalone VSlices iteration** conducted by one group, with one relevant Method Orientation and a revisable modality decision.  
**Source of proposal:** dialogue with Hernán (2026-10-12), following distinctions between Orientation, Work Forces, three candidate Paths and modality selection.  
**Owners:** TBD after evidence; the playground specification does not transfer conceptual ownership from Method or Design to Tooling.

## 1. Why explore this

The existing labels *Path of Most Value*, *Path of Most Continuity* and *Path of Least Resistance* may describe **orientations of effort** more faithfully than literal routes. *Value Orientations* is a **candidate working name** for a triangular visualization; it does **not** rename or replace existing [Path mechanism candidates](../../mechanisms/README.md).

Hernán's working interpretations, explicitly **not yet reconciled with current Path definitions**, are:

| Candidate value orientation | What is prioritized **while conducting the iteration** |
| --- | --- |
| **Most Value** | Short-term business value. |
| **Most Continuity** | Long-term business value, including establishing meaningful continuity between organizational processes and software where supported by the case. |
| **Least Resistance** | Business value with the least justifiable effort. |

These indicate **priorities governing the process**, not a retrospective classification by all benefits produced. A Least Resistance iteration might later yield long-term value without thereby having been directed by Most Continuity. An iteration may face competing priorities, but the triangle is not evidence that they form a mathematically complete or independent basis.

The [current candidate conceptual specification](../../mechanisms/value-orientations.md) now gives the **working collective name** *Value Orientations* to the three legacy Paths, while preserving their historical files and keeping the proposal under research. This playground is a potential realization of that candidate interpretation, not its semantic authority.

## 2. The first unit: standalone iteration only

Model **only the decision and development of one standalone group's iteration**.

Do **not** model:
- a parent VSlices iteration containing parallel or sequential child iterations;
- different groups each following separately weighted orientations under an overarching parent;
- aggregation of child outcomes, scores, statuses or modality recommendations;
- coordinated scheduling, authority propagation or dependency management across runs.

Such **composite executions** may later have their own parent orientation (e.g. a Most Value parent with Least Resistance and Most Continuity subgroups). That possibility is explicitly **future work**, not a case silently included in the current triangle.

## 3. Proposed interpretive pipeline

```text
Available evidence and work context
  - organization and development team's local/general knowledge or uncertainty
  - needs/problems/opportunities across the organization
  - process knowledge and traceability between organizational work and software
  - delivery, economic, resource, technical and institutional conditions
  - previous iteration's Validating retrospectiva and feedback responses (if any)
      ↓
Method Orientation (situate the work; recommended before/among iterations)
      ↓
Work Forces (candidate interpretation of evidence)
  - semantic
  - technical
  - delivery
  - resources
      ↓
Value Orientations (candidate relative emphasis among three criteria)
      ↓
Method Modality Selection (consider feasibility, alternatives and risks)
  - Context-First / Problem-First / Slice-First
      ↓
Design iteration produces new evidence
      ↓
Validating closes with retrospective artifacts and feedback responses
      ↓
next Method Orientation may revise forces, emphasis, and modality
```

This is a **proposed explanatory relationship**, not a proved causal chain or automatic rule. Contextual constraints (e.g. funding deadline) are not themselves organizational process knowledge; both may contribute different evidence. A need for broad knowledge does **not** make Context-First feasible where no suitable sources/experts exist. Likewise low general knowledge does **not** automatically prescribe Slice-First: safe locally bounded realization also needs evidence, capability and acceptable risk.

Orientation establishes what the group needs to know to choose how to proceed; it **is not disguised Context-First**. Design modalities advance the resolution. The [canonical lifecycle](../../products/design/lifecycle.md) and [Method Orientation](../../products/method/orientation.md) remain authorities for their respective meanings.

## 4. Triangle visualization (candidate)

Show three labeled vertices:

- **Most Value:** short-term business value.
- **Most Continuity:** long-term business value.
- **Least Resistance:** business value at minimal justified effort.

Show a position inside the triangle representing **proposed relative process emphasis**, with visible uncertainty and provenance. The position may move as evidence accumulates.

For a manual conceptual prototype, an operator may adjust three non-negative weights and normalize them *for display only* into barycentric coordinates. **These weights are illustrative inputs**, not measured facts, probabilities, semantic distances, validated priority scores or a mandatory sum-to-100 business rule. The interface must say this clearly.

For an evidence-based version, **do not assign numerical coordinates when evidence does not warrant it**. Provide a qualitative region, several plausible positions, an unknown state or refuse precise placement as appropriate. Do not hide ambiguity in a visually precise dot.

Visual history is useful when a new piece of evidence shifts interpretation: preserve previous and current position or regions, what changed, why it mattered, which source supports it, and whether the change reflects evidence, a correction or a changed intention.

## 5. Playground interactions

**Manual / earliest realization**
- Move the indicative position by adjusting the relative emphasis on the three orientations.
- Save a prior snapshot and visually compare changes.
- Attach a short reason or explicitly label the change as a simulation.
- Explore cases and counterexamples; no automatic or validated recommendation implied.

**Evidence-assisted / later experiment**
- Supply selected documents or snapshots **with provenance**, dates, scope and relevant actor/authority.
- Distinguish observed excerpts from model interpretations about local/general uncertainty, needs, constraints and Work Forces.
- Produce a status: supported/contested/unknown claims, reasons for inferred forces, qualitative orientation emphasis, limits and missing evidence.
- Offer a **candidate** modality recommendation **with alternatives**, feasibility conditions, risks, counterevidence and explanation of why another modality is less supported.
- Reassess on new documents or retrospectives: display differences and their source, without silently rewriting previous states.
- Allow an authorized actor to correct evidence interpretation and decide a modality; the LLM is an assistant, not the owner of that decision.

**Potential LLM integration**
- Retrieval and source citation, extraction, temporal ordering, explicit contradiction detection, comparison of hypotheses and grounded explanation.
- Structured provisional outputs are possible, but their shape/ontology requires empirical refinement; **do not claim an adopted JSON schema, scoring formula or inference algorithm yet**.
- Keep prompt inputs, model-inferred claims, user corrections, chosen modality and eventual outcome distinguishable for audit/replay.
- No automatic repository changes, deployment, scheduling or invocation of Design iterations from a recommendation.

## 6. Hypotheses and falsification

Candidate hypotheses for a research-oriented evaluation:

1. Work Forces provide an **interpreted view of evidence** relevant to Value Orientations, rather than acting as synonyms for the orientations.
2. Three orientations can help explain **process priority** for a standalone iteration without equating that priority with resulting benefits.
3. Their evidence-sensitive combination improves the discriminating justification of a Method modality recommendation over current selection guidance alone.
4. The triangle remains meaningful even when relative emphasis cannot be estimated numerically.

Adversarial cases to retain:
- High general uncertainty **without** access to organizational experts or reliable sources: Context-First may be blocked, not automatically selected.
- Low general knowledge with strong local knowledge: Slice-First may be viable **only if** a small bounded action is responsible.
- An urgent business problem with a deadline: the pressure may favor Problem-First, Slice-First, neither or a bounded combination of work; do not presuppose a fixed mapping.
- Well-understood organizational processes but weak traceability to software: Context-First can still advance development by establishing that connection.
- Two distinct mechanisms suggest the same modality for different reasons: require evidence to differentiate claims.
- Evidence that does not discriminate among regions or modalities: show indeterminacy rather than invent a recommendation.

A fixed affinity of the three corners with the three modalities is **a hypothesis to test**, not a mapping codified by this playground. The extreme-case intuition described by Hernán is an important study target, not yet a validated universal rule.

## 7. Acceptance criteria for a future first implementation

- A user can manipulate one standalone group's triangle and compare at least two states.
- The UI explicitly labels manual inputs and sample numbers as hypothetical.
- The representation of current state, previous state and reasons for a change remains discernible.
- No implication that the visual is a validated quantitative method.
- A future evidence-assistance view clearly differentiates sources, interpretations, missing evidence and a provisional recommendation.
- The UI never treats the LLM's proposed modality as an authorized decision.
- No composite/nested orchestration, automated iteration execution, or required new canonical mechanism.

## 8. Sources, governance and open design questions

- [Current candidate Paths](../../mechanisms/README.md) — existing labels and definitions remain unchanged.
- [Work Forces](../../forces/README.md) — candidate pressure groups.
- [Action Flow](../../mechanisms/action-flow.md) — work elaboration and transformation space; may be a useful source of evidence but is **not** the triangle.
- [Method Orientation](../../products/method/orientation.md), [Modality Selection](../../products/method/modality-selection.md) and [Modality Switching](../../products/method/modality-switching.md).
- [Design modalities](../../products/design/README.md) and [Design lifecycle](../../products/design/lifecycle.md).
- [Reasoning reconstruction gap](../../mechanisms/reasoning-reconstruction-gap.md) and [Research Input #23](https://github.com/vslices/research-space/issues/23).
- Historical [VSlices Method modality selection](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-selection.md) and [Design modality comparison](https://github.com/vslices/docs/blob/main/es/products/design/modalities/comparisons.md).

Open: correct name; conceptual ownership of Value Orientations; relationship to existing Path meanings; whether three criteria suffice or overlap; evidence-to-force-to-position interpretability; qualitative versus quantitative display; validity of extreme-case affinities; how to assess useful recommendations without letting outcomes rewrite the original process criterion; what an eventual composition model would require.

**This specification is intentionally a testable proposal, not a completed product or a promotion of research findings.**
