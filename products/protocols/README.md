# VSlices Protocols

**Conceptual owner:** VSlices Protocols  
**Status:** product-boundary consolidation, 2026-10-11; individual protocols retain their own maturity and evidence.

## Official repository and planned rename

- **Current official specialized source:** [`vslices/planifications`](https://github.com/vslices/planifications).
- **Planned repository rename:** **`vslices/planifications` → `vslices/protocols`**.
- **Rename status:** **planned, not executed** as of this review. Links to `vslices/planifications` refer to the real current repository; do not assert that `vslices/protocols` already hosts anything.
- **Conceptual identity:** VSlices Protocols. The former term *Planifications* remains useful as historical repository naming and for particular planning artifacts; it does not exhaust this product's responsibility.

A future physical rename should preserve Git history, existing references, consumers and protocol identity, and review links in the Suite, agents, Tooling integrations and other VSlices repositories. Renaming the repository is **not** a license to rename protocol identifiers or rewrite frozen execution evidence.

## Purpose

**VSlices Protocols defines reusable, executable procedures for coordinating work from a real objective and available evidence toward bounded decisions, actions, observations, validation and responsible continuation.**

It describes **when and why a procedure applies, how to traverse it, how it delegates to the relevant semantic and technical owners, what evidence is needed to proceed or stop, and how execution remains reconstructible** across actors and sessions.

It does not define a universal implementation architecture, the semantics of the work being performed, the Design lifecycle, or the meanings of VSlices products. A protocol's value lies in its **operable coordination and learnable reuse**, not the number of prescribed documents or steps.

The source problem remains primary. Protocol evolution should be driven by observed pressure in real work rather than by the desire to create a complete procedural hierarchy.

## Useful distinctions

| Concept | Responsibility |
| --- | --- |
| **Protocol** | A reusable procedure with a recognizable purpose, conditions for invocation, relevant decisions and authority, progression, evidence, and continuation/exit behavior. Its exact detail is proportional to the work. |
| **Meta-protocol** | A protocol coordinating discovery, selection, delegation, evolution and continuation of other bounded procedures or plans while preserving the owning task. |
| **Plan / planification** | A bounded working strategy or traversal for a particular kind of effort, which a protocol can use without converting all plans into meta-protocols. The existing *Progressive Source Migration* is one witness. |
| **Execution run** | An authorized application to concrete work; its state, actions and evidence are not the reusable protocol definition. |
| **Protocol supervision / review** | A distinct observational responsibility about an execution and protocol behavior. Its findings must not be confused with the executor's own actions, the consumer's facts, or a Research study. |

These are **working distinctions**, not a compulsory taxonomy of file types or a requirement that every protocol have every element represented in a separate artifact.

## Responsibility boundaries

- **VSlices Suite:** owns cross-product principles, including [grounded projection](../../README.md#suite-principle--grounded-projection). The results of protocol work should remain explainable from understood problems and justified requirements.
- **Design:** owns working methodologies, Context-/Problem-/Slice-First **definitions**, and the five-phase iteration: **Understanding → Contextualizing → Planning → Building → Validating → Understanding**. [Validating](../design/lifecycle.md) contrasts outcomes, incorporates evidence and **responds to feedback if received**, producing retrospective artifacts and feedback responses that close the iteration and inform the following Method Orientation.
- **Method:** owns [Orientation](../method/orientation.md), **recommended at process start and between iterations when using Method and fed by the previous Validating outputs**, coordination among VSlices product responsibilities, and contextual [modality selection](../method/modality-selection.md) / [switching](../method/modality-switching.md). A protocol can enact these decisions; it does not redefine their meaning.
- **Docs Standard:** owns documentary artifact semantics, question roots and Continuity Paths. Protocols decide when and how to use those definitions, not their semantic content or mandatory production.
- **Template Standard:** owns representation/reconstruction contracts; **Tooling** provides executable mechanisms; **Ruleset** owns target-specific realization vocabulary; **Intermediate Representation** owns VSIR semantics; **Framework** owns its own software-semantic concepts.
- **Consumer repository:** owns the actual software/work, executed changes, product evidence and authorized executor state. Research owns separate studies and promoted research evidence.

**Current pressure → needed responsibility → relevant owning surface, when any** is a stronger discovery rule than requiring every run to visit all VSlices products.

## Evidence, autonomy and learning

The existing protocols demonstrate reusable concerns, **not universal mandatory gates**:

- Distinguish observed, inferred, provisional, confirmed, unknown, contradicted and rejected claims/decisions according to the claim's evidence and authority.
- Route questions separately to those **who know**, **who may decide** and **who can observe or validate**; technical execution capacity alone is not domain or institutional authority.
- Let Building and other concrete action produce evidence and safely resolve bounded/reversible uncertainty. Revisit earlier decisions when meaning, scope, authority or costly boundaries change.
- Use the smallest justifiable procedure or next action; prefer links to source, code, tests, runtime and commits over duplicate narrative.
- Preserve material stage/decision closure, changed supervision arrangements and recovery evidence without pretending omitted work occurred.
- Treat a protocol failure or gap as evidence for possible improvement, not automatic permission to redefine another product.

## Current official corpus and maturity

### In `vslices/planifications/main`

- [VSlices Usage](https://github.com/vslices/planifications/blob/main/protocols/vslices-usage/README.md): shared operational entrypoint, minimal orientation, work geometry and routing. **Its Feedback-based traversal is historically provisional and conflicts with the subsequently approved Design lifecycle**; it must be reconciled rather than treated as authority over Design.
- [Docs Standard Usage](https://github.com/vslices/planifications/blob/main/protocols/vslices-docs-standard-usage/README.md): documentary application beginning from continuity pressure, not a required artifact list. Some historical public artifact references need re-routing to official current Docs Standard definitions.
- [Docs Standard Extension](https://github.com/vslices/planifications/blob/main/protocols/vslices-docs-standard-extension/README.md): procedure for bringing evidence-backed extension pressure to the owning artifact family, without assuming candidate definitions are installed/promoted.
- [Tooling Usage](https://github.com/vslices/planifications/blob/main/protocols/vslices-tooling-usage/README.md): an intentionally incomplete operational handoff pending concrete supported Tooling capabilities.
- [Software Migration](https://github.com/vslices/planifications/blob/main/protocols/software-migration/README.md): meta-protocol for migration, decision-specific authority, bounded Planning-to-Building, source evidence, reversible uncertainty, state/placement, findings and evolution. Its Research-based revision was [merged in PR #2](https://github.com/vslices/planifications/pull/2) on 2026-10-09; its effectiveness still needs execution evidence/replay.
- [Progressive Source Migration](https://github.com/vslices/planifications/blob/main/plans/progressive-source-migration.md): experimental, specialized reconstruction plan, not the full identity of Protocols.

### Distinct candidate branches, **not** integrated into `main`

- [Software Development — PR #3](https://github.com/vslices/planifications/pull/3), branch `feat/software-development-meta-protocol`: candidate meta-protocol, startup/state, execution bootstrap, supervision bootstrap, run convention and protocol-design considerations. It uses approved **Validating** and Method-owned situational Orientation, and contains initial supervision witnesses from a TDidacta Platform development run. The existence of a run **does not yet validate the whole meta-protocol**.
- [Executable Discovery — PR #1](https://github.com/vslices/planifications/pull/1), branch `feat/executable-discovery`: experimental bounded observation of existing software to reconstruct organizational work using execution evidence, not simply regression testing.
- [Protocol Design](https://github.com/vslices/planifications/blob/feat/software-development-meta-protocol/protocols/protocol-design/README.md) and [considerations](https://github.com/vslices/planifications/blob/feat/software-development-meta-protocol/protocols/protocol-design/considerations.md): candidate evidence-based internal procedure for creating/updating protocols; belongs operationally to Protocols, **not** to Design's ownership of methodologies.

## Execution and supervision provenance

The general rule supported by Software Migration and Software Development is: **primary execution evidence and executor state belong to the consumer/source repository**, not the reusable definition repository. Resume existing authorized runs rather than create duplicates.

The candidate [protocol run convention](https://github.com/vslices/planifications/blob/feat/software-development-meta-protocol/protocols/run-convention.md) distinguishes a different responsibility: **protocol-owned supervision, observation and review records** may live within that protocol under `protocols/<protocol-id>/run/<run-id>/`, linking the consumer evidence. These are not competing executor states, automatic Research studies or a requirement to move existing runs. This convention is still on a candidate branch.

Preserve actual authorization, execution placement and primary witnesses. A command that *should* succeed is not an executed result.

## Open reconciliation and next decisions

1. **Naming:** implement the planned `vslices/planifications` → `vslices/protocols` repository rename separately, with reconstructible references and without rewriting historic protocol runs.
2. **Lifecycle:** align shared Usage and older migration/Docs Standard procedures with the canonical five-phase **Design** cycle and **Method** Orientation; maintain historical provenance rather than silently calling Feedback a sixth/alternate phase.
3. **Documentary semantics:** replace legacy public Docs Standard taxonomy and path-priority assumptions in operational references with links to current owning definitions; do not mandate all Paths or create fixed path rankings.
4. **Source-of-truth boundary:** keep a compact product definition here and the detailed protocol definitions in the official specialized repository, allowing those definitions to evolve without mirroring them in Suite.
5. **Run conventions:** evaluate the candidate separation between consumer execution and protocol-owned supervision during real use. Do not treat a new convention as already universally adopted.
6. **Shared procedures:** Software Development and Migration may reuse genuine responsibilities, but similarity alone does not justify extracting a global child protocol or duplicating Method/Design.
7. **Plans versus protocols:** review the remaining `plans/` namespace after the rename to decide whether it remains useful; do not reclassify or delete historical plans just to make the repository name uniform.

## Provenance

Primary sources: [repository README](https://github.com/vslices/planifications/blob/main/README.md), [AGENTS](https://github.com/vslices/planifications/blob/main/AGENTS.md), [VSlices Usage](https://github.com/vslices/planifications/blob/main/protocols/vslices-usage/README.md), [Software Migration](https://github.com/vslices/planifications/blob/main/protocols/software-migration/README.md), [PR #2](https://github.com/vslices/planifications/pull/2), [Software Development PR #3](https://github.com/vslices/planifications/pull/3), [Executable Discovery PR #1](https://github.com/vslices/planifications/pull/1), and canonical Suite [Design](../design/lifecycle.md) / [Method](../method/orientation.md).

This definition records present responsibility and planned naming. It **does not itself rename GitHub repositories, merge candidate PRs or authorize new consumer runs**.
