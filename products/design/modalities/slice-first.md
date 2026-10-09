# Slice-First — VSlices Design modality

**Owner:** VSlices Design  
**Status:** canonical migration of existing Design modality semantics, aligned with the approved five-phase lifecycle (2026-10-09).

## Definition

**Slice-First** prioritizes learning through a **small, meaningful, end-to-end vertical slice**, when implementation and observation can safely resolve relevant uncertainty sooner than extended prior analysis.

It deliberately keeps initial contextual investigation narrow **but sufficient to avoid blind implementation**. The slice is an instrument for learning, not an automatic commitment to a final architecture or product. Smallness concerns the **smallest meaningful route from intent to observable evidence**, not merely few lines of code.

The work must know what it seeks to learn, which assumptions and risks it accepts, how the outcome could challenge the chosen direction, and what may need to be discarded or reversed.

## Emphasis in the approved five-phase Design lifecycle

| Phase | Slice-First emphasis |
| --- | --- |
| **Understanding** | Bounded: identify the intended learning, affected actors, essential domain concepts, assumptions and safety limits. |
| **Contextualizing** | Bounded: establish the smallest meaningful context, flow, boundaries and dependencies that support the slice without misleading interpretation. |
| **Planning** | Focused: choose the smallest significant end-to-end slice, its testable assumptions, expected observations, exclusions, risks and reversal conditions. |
| **Building** | Strong: realize the slice, encounter integration and runtime constraints, and collect implementation evidence. Building may expose mistaken assumptions. |
| **Validating** | Strong: contrast observed outcomes against learning intent, problem understanding, acceptance criteria and consequences; **respond to feedback if received**. Distinguish what the slice actually demonstrated from what remains untested. |

Slice-First uses the **same five Design phases**, not an alternative process. Strong Building and Validating emphasis does not eliminate Understanding or Contextualizing.

## When this emphasis is useful

Indicators include:
- enough domain and problem context to bound a meaningful, safe experiment;
- a specific technical/product uncertainty that functioning software could expose;
- a small end-to-end behavior able to test the intended assumption;
- bounded or reversible cost of being wrong;
- a realistic way to observe the result rather than merely demo it;
- further upfront analysis unlikely to improve the next decision as much as implementation evidence.

These are **indicators of fit**, not an automatic Method selection rule. Slice-First may be unnecessary when a well-understood change can simply be implemented without a learning slice.

## Adequacy and risks

The slice should make explicit **what it can and cannot establish**. A working prototype may prove that one path functions without proving domain correctness, production readiness, user value, operational resilience or suitability of the broader architecture.

Material risks include:
- implementing on weak business assumptions;
- expanding scope through adjacent flows or dependencies;
- accidental architectural commitments or prototype code made permanent;
- insufficient error handling or operational constraints;
- overinterpreting early feedback or a technically successful demo;
- stakeholders mistaking an experiment for a finished solution;
- irreversible or high-cost effects hidden behind a supposedly small slice.

The modality loses its justification if the context needed to act safely is not sufficiently understood, reversibility is inadequate, or the resulting evidence cannot be meaningfully evaluated. In those circumstances Method may reconsider Problem-First or Context-First. No transition is mandatory or ordered.

## Responsibility boundary

- **Design** owns this modality's meaning, learning emphasis, relation to the five phases, conditions and risks.
- **Method** owns selecting, continuing or changing modalities under actual uncertainty, priorities and continuity. See [Modality Selection](../../method/modality-selection.md) and [Modality Switching](../../method/modality-switching.md).
- **Planifications** may coordinate procedural application and state without defining the modality.
- **Docs Standard** may provide structures for learning intent, assumptions, outcomes or decisions when preservation is material; no fixed set of documents is required.

## Provenance and migration notes

Historical published sources:
- [Slice-First overview](https://github.com/vslices/docs/blob/main/es/products/design/modalities/slice-first/index.md)
- [Slice-First iteration emphasis](https://github.com/vslices/docs/blob/main/es/products/design/modalities/slice-first/iteration-flow.md)
- [Slice-First risks and relations](https://github.com/vslices/docs/blob/main/es/products/design/modalities/slice-first/risks-and-relations.md)

**Retained:** intentional minimum context; end-to-end learning slice; high Building emphasis; explicit assumptions, reversibility and exclusions; observable evidence; risks of accidental production permanence; no fixed modality progression.

**Adapted explicitly:** the historical four-phase presentation placed building, delivery, validation and feedback together in **Building**. In the [approved Design lifecycle](../lifecycle.md), **Building** realizes and can discover evidence while **Validating** is a separate fifth phase that contrasts outcomes and **responds to feedback when provided**. A slice does not require unsolicited feedback to exist, but must offer a meaningful way to evaluate what was learned.

Historical language about deciding to switch modalities is retained as evidence and indicators, while the contextual decision is owned by **Method**, not the definition of Slice-First.

**Not added:** mandatory experimentation checklists or templates, numerical risk thresholds, a guarantee that every slice must reach production, an exhaustive definition of external validity, or ownership of Orientation.
