# Orientation — VSlices Method

**Semantic owner:** VSlices Method  
**Status:** agreed conceptual responsibility (2026-10-09); detailed procedures and authority-resolution rules remain candidates.

## Definition

**Orientation** is the Method responsibility through which **actors and teams recover, contrast and update their situated position relative to the continuity of work**—its intentions, current state, decisions, evidence, responsibilities, uncertainty and dependencies—**so their next participation can be responsible**.

Orientation mediates between inherited work state and present participation **regardless of how complete, interrupted, resumed or closed Design iterations are**.

## Anti-corruption boundary

The *anti-corruption layer* analogy identifies a semantic protection, not necessarily a software component: **do not automatically translate inherited work state into present truth or present authority**.

Orientation should distinguish:
- what was observed, what was interpreted, what was decided and what is now justified;
- historical commitments from still-applicable commitments;
- documented agreement from unresolved differences;
- work state from the actor's knowledge of that state;
- knowing about a decision from being authorized to change or execute it.

Its purpose is **not** to reject history, rebuild everything or require proof of each inherited fact. Recover and examine only the continuity material to a responsible next action. Uncertainty may be broader than the bounded work an actor can safely undertake.

## Two connected perspectives

**Actor orientation:** what this actor currently knows, does not know, is responsible for, may decide, depends on and can contribute. An actor's understanding is not automatically collective agreement.

**Team orientation:** what understanding and decisions are shared, where perspectives diverge, who holds relevant authority, which responsibilities are coordinated and which uncertainties affect collective work. A team's shared position does not confer every authority on every actor.

The perspectives inform one another **without collapsing into a single perspective**. An individual discrepancy may warrant shared review; a changed shared decision may require actors to reorient. Neither is universally automatic.

## When Orientation matters

Possible occasions include joining work, resuming after interruption, inheriting a partial iteration, a consequential change in participants or responsibilities, contradictions among artifacts and behavior, an external change, or evidence produced by Building/Validating.

**Orientation is not a sixth Design phase**, nor a mandatory gate before every phase or iteration. It may occur mid-iteration and may conclude that the responsible next action is to continue, consult a source or authority, revisit an assumption, select or switch a Design modality, refrain from implementation, or preserve an explicit disagreement.

## Boundaries and relationships

- **Design** owns Understanding, Contextualizing, Planning, Building and Validating. Understanding investigates the problem and work; **Orientation situates participants in the ongoing continuity of work**. They may exchange evidence without being interchangeable.
- **Design Validating** contrasts outcomes with understanding, expectations, criteria and consequences and responds to feedback if received. Its evidence **may justify reorientation**; it does not automatically perform or require complete reorientation.
- **Method Modality Selection / Switching** choose Design emphasis in present circumstances; Orientation may supply situated evidence but is neither identical to selection nor required to terminate in a modality choice.
- **Method Context Guides** suggest how Method can approach recognizable contexts (e.g. joining existing work); they do not define the actor's actual situated position.
- **Docs Standard** can preserve decisions, provenance, questions and continuity using its own structures. A particular Orientation document is not required.
- **Planifications** may operationalize reorientation or recovery in concrete runs, without redefining this Method responsibility.

## Adequacy and limits

Sufficient orientation makes the next participation explicable in terms of relevant intent, evidence, responsibilities, uncertainty and consequences **without pretending to possess missing knowledge or authority**.

It does not require a synchronized universal state, comprehensive onboarding, complete iteration closure, consensus, or immediate resolution of all disagreements.

An unresolved design question is **when divergence between actor and team perspectives warrants revising shared orientation rather than preserving the divergence locally**. That depends on decision impact, authority and evidence; do not invent an automatic rule.

## Decision lineage

1. Earlier Suite discussions placed an explicit **Orientation** around an extended cycle: `Orientation -> Understanding -> Contextualizing -> Planning -> Building -> Feedback -> Orientation`. That model made continuity visible but blurred Design and Method.
2. Design approved the five-phase cycle `Understanding -> Contextualizing -> Planning -> Building -> Validating -> Understanding` and left Orientation ownership open.
3. The migrated Method [Context Guides](context-guides/README.md), particularly [Joining Existing Work](context-guides/joining-existing-project.md), exposed a distinct need to locate the participant relative to ongoing work without redoing Design's problem investigation.
4. Review identified Orientation's role as a semantic anti-corruption boundary between inherited iteration state and responsible present participation, independent of iteration completeness, and distinguished mutually informing actor/team perspectives.
5. **Current position:** Orientation is a Method-owned cross-cutting responsibility, **not a Design phase**. Operational mechanisms and perspective-reconciliation thresholds remain unapproved.

Historical evidence: [public Method overview](https://github.com/vslices/docs/blob/main/es/products/method/index.md), [Joining Existing Project](https://github.com/vslices/docs/blob/main/es/products/method/context-guides/scenarios/joining-existing-project.md); [Design lifecycle](../design/lifecycle.md). This source states a revised decision; it does not retrofit that decision into the historical texts.
