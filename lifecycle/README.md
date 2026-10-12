# Lifecycle — Suite relationship and historical surface

**Authoritative Design phase definitions:** [VSlices Design lifecycle](../products/design/lifecycle.md). This Suite page tracks history and cross-product interpretation; when wording differs, the Design-owned source controls Design phase meaning.

## Status and authority

The **five-phase Design iteration** and the definition of **Validating** below are **conceptually approved (2026-10-09)**. This file preserves the Suite's cross-product relationship to the Design-owned concept; it must not make the Suite the permanent substitute for a Design-owned canonical surface.

**Design owns** the phases and their meanings, as well as the definitions of Context-First, Problem-First and Slice-First. **Method owns** contextual selection or switching of modalities according to uncertainty, priorities and continuity; **Protocols** operationalizes them in runs (the specialized repository is currently named `vslices/planifications`).

Orientation is intentionally **outside** the five-phase Design iteration and is [Method-owned](../products/method/orientation.md). It situates actors and teams relative to the continuity of work regardless of iteration completeness. Entry/re-entry triggers and the operational reconciliation of actor/team perspectives remain subject to evidence and review; Validating may produce a reason to reorient, but does not mandate a sixth Design phase.

## Approved Design iteration

```text
Understanding -> Contextualizing -> Planning -> Building -> Validating
       ^                                             |
       +---------------------------------------------+
```

The cycle's earlier evolution must remain reconstructible:

1. **Historical, four-phase**: Understanding -> Contextualizing -> Planning -> Building -> Understanding.
2. **Intermediate candidate**: Orientation -> Understanding -> Contextualizing -> Planning -> Building -> Feedback -> Orientation.
3. **Approved conceptual correction**: the five Design phases end with **Validating**, then iterate to Understanding; Orientation is distinguished from those five, and feedback is a possible input to Validating rather than a required independent phase.

This is a conceptual decision, not evidence that all existing tools, plans or public pages already conform.

## Orientation — Method-owned; operational details open

[Method Orientation](../products/method/orientation.md) mediates between inherited work state and responsible present participation, distinguishing an actor's own position from shared team understanding and authority. It can matter when joining, resuming, changing scope or participants, or discovering contradictory evidence—even during an unfinished Design iteration. Evidence from Validating may justify refresh without making it automatic. Its **conceptual owner is settled**; specific operational triggers and methods of reconciling perspectives are still candidates.

## Understanding

Understanding focuses on work and meaning before system realization.

Current rule candidate:

> Understanding produces or deepens **Abstract Action Flows**, not system Action Flows.

It seeks to understand:

- work;
- concepts;
- actors;
- conditions;
- cardinality;
- consequences;
- uncertainty;
- relevant business context.

## Contextualizing

Contextualizing deepens abstract understanding and places it in surrounding context.

It may begin organizing knowledge according to possible realization without requiring a complete implementation model.

Relevant context may include:

- areas;
- departments;
- actors and roles;
- existing systems;
- current boundaries;
- responsibilities;
- dependencies;
- current pain;
- candidate realization pressures.

## Planning

Planning changes the primary focus from abstract work toward proposed realization.

It may:

- identify semantic responsibilities;
- propose candidate system boundaries;
- compare alternatives;
- use technical criteria such as coherence, cohesion, and coupling;
- consider dominant work forces;
- produce candidate Systematized Action Flows.

Planning need not finalize every implementation detail.

## Building

Building completes the realization decisions that only implementation pressure can reveal and develops the proposed system.

Implementation is evidence.

Building may confirm, refine, or contradict earlier understanding.

## Validating — approved meaning

**Validating contrasts iteration results with the understanding of the problem, expectations, acceptance criteria, and observed consequences.** It incorporates new evidence, identifies discrepancies, and **responds to feedback received, when feedback exists**.

Its results may confirm, challenge, or change the understanding, decisions, and realizations that motivated the iteration. Responding to feedback does **not** require accepting it automatically: an adequate response may accept an observation, explain or justify a decision, identify uncertainty, propose a change, or explain why a change is not warranted.

Validating is not limited to technical verification. Feedback is an optional input, not a guaranteed event and not a mandatory separate Design phase. Evidence from Validating may inform the next Understanding iteration and any orientation refresh.

## Distinct concerns

- **Design lifecycle**: meaning of the five phases and iterative return.
- **Design modalities**: meaning of Context-First, Problem-First, Slice-First.
- **Method**: given uncertainty, priorities and continuity, select or change modality and coordinate participating VSlices responsibilities.
- **Protocols** (currently `vslices/planifications`): operational execution, state and traceable application of this guidance.
- **Orientation (Method)**: cross-cutting situated continuity for actors and teams; its operational procedures remain revisable.
