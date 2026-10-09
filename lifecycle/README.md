# Lifecycle — Suite relationship and historical surface

**Authoritative Design phase definitions:** [VSlices Design lifecycle](../products/design/lifecycle.md). This Suite page tracks history and cross-product interpretation; when wording differs, the Design-owned source controls Design phase meaning.

## Status and authority

The **five-phase Design iteration** and the definition of **Validating** below are **conceptually approved (2026-10-09)**. This file preserves the Suite's cross-product relationship to the Design-owned concept; it must not make the Suite the permanent substitute for a Design-owned canonical surface.

**Design owns** the phases and their meanings, as well as the definitions of Context-First, Problem-First and Slice-First. **Method owns** contextual selection or switching of modalities according to uncertainty, priorities and continuity; **Planifications operationalizes** them in runs.

Orientation is intentionally **outside** the five-phase Design iteration. Its final conceptual ownership (Method vs Design), initial entry behavior and refresh mechanism have **not** been approved as a stable assignment. The current working hypothesis is an initial orientation when joining a project and refresh informed by Validating, without a sixth Design phase.

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

## Orientation — ownership not yet settled

Orientation establishes sufficient entry continuity when entering existing work. Validating can provide evidence that the orientation needs refreshing; whether refresh is a Method action, a Design action, or an operational consequence of the run remains under review. **Do not** represent Orientation as an automatic sixth Design phase or claim an agreed owner.

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
- **Planifications**: operational execution, state and traceable application of this guidance.
- **Orientation**: entry and continuity concern whose *ownership remains under review*.
