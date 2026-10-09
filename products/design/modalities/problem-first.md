# Problem-First — VSlices Design modality

**Owner:** VSlices Design  
**Status:** canonical migration of existing Design modality semantics, aligned with the approved five-phase lifecycle (2026-10-09).

## Definition

**Problem-First** starts with a **specific visible problem, pain, limitation or opportunity** and develops **enough surrounding context** to understand it and pursue a justified improvement.

A reported problem is a **starting signal**, not an unquestionable diagnosis. The work must distinguish the problem from its label, symptoms, possible causes, affected actors, dependencies and consequences. Nor does the presence of a problem automatically justify a software solution.

The modality focuses inquiry rather than expanding it across the whole domain in advance. Its risk is not primarily ignorance of the entire domain, but **misunderstanding the particular problem or optimizing locally at the expense of adjacent work**.

Its balance is between enough contextual grounding and sufficiently early progress on a responsible response.

## Emphasis within the approved Design cycle

| Phase | Problem-First emphasis |
| --- | --- |
| **Understanding** | Focused: investigate who experiences the problem, when and how it arises, related concepts and competing explanations, including whether the reported problem is only a symptom. |
| **Contextualizing** | Focused: place the problem in its current flows, relevant actors, responsibilities, rules, dependencies and adjacent consequences; widen context when it can change the decision. |
| **Planning** | Strong: compare candidate improvements, expected outcomes, accepted risks, scope, feasibility, tradeoffs and alternatives, without selecting the first appealing fix. |
| **Building** | Realize or test the response while tracing it to the problem, affected work, expected improvement and accepted risks. Implementation may expose missing knowledge or revise decisions. |
| **Validating** | Contrast observed outcomes against the understanding of the problem, expected improvements, acceptance criteria and consequences. Incorporate evidence, identify discrepancies and **respond to feedback if received**; determine whether the problem actually improved. |

Problem-First uses the same five Design phases as other modalities. It **emphasizes Planning** while maintaining sufficient Understanding and Contextualizing; it does not skip them or add its own stages.

## When the emphasis is useful

Examples of relevant evidence:

- a recurring pain or bottleneck has become visible;
- affected actors or an area of impact can be identified;
- the surrounding domain is sufficiently known to begin focused inquiry;
- the cause, boundary, impact or expected improvement still needs examination;
- a bounded change may affect nearby flows, rules or responsibilities;
- broad domain discovery would currently add less value than careful problem investigation.

These are **indicators**, not a mandatory selection checklist. **Method owns the contextual decision** to select, continue or change modalities.

## Adequacy, risks and stopping

Problem-First seeks a sufficiently well-explained problem and enough surrounding context to compare and assess responsible options. It does **not** require mapping the entire domain or making Planning an exhaustive implementation blueprint.

Material failure modes include:

- mistaking the first problem statement for a verified cause;
- solving a visible symptom while preserving the underlying problem;
- optimizing one workflow while harming another;
- ignoring hidden dependencies or ownership;
- selecting a technical response before clarifying the intended improvement;
- poorly defined success evidence or unexamined accepted risks;
- overfitting an implementation to one visible case.

If the problem cannot be understood without substantial surrounding context, Method may reconsider **Context-First**. If a small, reversible realization can now supply the most useful evidence, Method may reconsider **Slice-First**. Neither transition is automatic and no sequence is required.

## Ownership relationships

- **Design** defines the meaning, focus, strengths and risks of Problem-First and the meanings of the five phases.
- **Method** selects or switches Design modalities according to uncertainty, priorities and continuity; see [Modality Selection](../../method/modality-selection.md) and [Modality Switching](../../method/modality-switching.md).
- **Planifications** coordinates concrete application without redefining the modality.
- **Docs Standard** provides optional structures to preserve knowledge where needed; a fixed document inventory is not a requirement of Problem-First.

## Provenance and migration decisions

Historical public sources:

- [Problem-First overview](https://github.com/vslices/docs/blob/main/es/products/design/modalities/problem-first/index.md)
- [Problem-First iteration flow and emphasis](https://github.com/vslices/docs/blob/main/es/products/design/modalities/problem-first/iteration-flow.md)
- [Problem-First risks and relations](https://github.com/vslices/docs/blob/main/es/products/design/modalities/problem-first/risks-and-relations.md)

Preserved: starting from a specific problem, obtaining enough context, focused Understanding and Contextualizing, strong Planning, proportional solutions, visible risks, avoidance of symptom-solving and local optimization, and the ability to change modalities.

Explicit adaptation: historical material presented validation, delivery and feedback within **Building** and an automatic return to Understanding under the earlier four-phase model. Under the [approved five-phase Design lifecycle](../lifecycle.md), **Validating** independently contrasts outcomes and **responds to feedback when provided**. Building remains a source of new evidence, not the owner of the complete Validating responsibility.

Selection and switching descriptions in historical Design pages are treated as indicators of fit, **not** a transfer of Method's authority to decide changes.

Not established here: mandatory problem-interview scripts, checklists, fixed artifact inventories, automatic transition thresholds, a complete Slice-First definition or the final owner of Orientation.
