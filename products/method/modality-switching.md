# Modality Switching — VSlices Method

**Owner:** VSlices Method  
**Status:** canonical migration of the existing Method pattern (2026-10-09); not a new process or a mandatory sequence.

## Purpose

**Modality Switching** determines when the current emphasis on a VSlices Design modality should change because learning has changed the uncertainty, priorities, or continuity that matter to the next responsible decision.

> Switch modalities when the current modality no longer helps reduce the dominant uncertainty.

A switch does not prove the previous modality was wrong. It may be evidence that the previous emphasis generated enough knowledge to continue differently. Modalities are not fixed identities of an iteration, stages of a process, or a ladder that must be completed in order.

## Typical transitions

These are illustrative decisions, not an exhaustive transition machine.

| From | To | Situation and purpose |
| --- | --- | --- |
| Context-First | Problem-First | Enough surrounding context is understood to focus on a specific pain, opportunity, or decision worth resolving. |
| Context-First | Slice-First | Context supports a bounded, reversible realization that can produce useful evidence. |
| Problem-First | Context-First | The apparent problem depends on surrounding work, actors, vocabulary, or constraints still misunderstood. |
| Problem-First | Slice-First | A sufficiently understood problem can now be tested through a small concrete realization. |
| Slice-First | Problem-First | The slice reveals that the problem was incomplete, misplaced, or misunderstood. |
| Slice-First | Context-First | Building or Validating reveals missing domain context, hidden actors, boundaries, or unexpected consequences. |

## Signals to reconsider

Possible signals include:

- new domain concepts appearing during implementation;
- repeated debate without new knowledge;
- a technically working slice that does not improve real work;
- a seemingly bounded problem whose surrounding workflows are poorly understood;
- growing documentation without safer decisions;
- received feedback or observed consequences contradicting assumptions;
- the same uncertainty recurring between activities;
- inability to explain why the current work matters.

These signals **prompt review**, not an automatic switch.

## How a responsible switch works

Re-examine what changed, which uncertainty now matters most, whether the current modality still helps, and what smallest next movement is likely to improve the decision. Preserve the reason for switching **only to the extent needed for future continuity**.

A switch may involve changing the next conversation, redirecting investigation, adjusting a design artifact, narrowing an experiment, or reopening a decision. It need not restart the Design iteration or require a new document.

## Tradeoffs and failure modes

- Keeping Context-First too long can prolong discovery without deciding what to validate.
- Keeping Problem-First too narrowly can disconnect a problem from its context.
- Keeping Slice-First despite warning signs can turn experimentation into implementation without adequate understanding.
- Switching too often can prevent sufficiently deep work.
- Never switching may preserve a mode that no longer serves the next decision.
- Switching without retaining material learning can force repeated rediscovery.
- Treating a switch as failure discourages useful feedback; treating it as a compulsory stage invents ceremony.

## Responsibilities

- **Design** owns the meanings and emphases of Context-First, Problem-First and Slice-First, and the five phases Understanding, Contextualizing, Planning, Building and Validating.
- **Method** owns the judgment to select, continue or switch the modality according to current evidence, uncertainty, priorities and continuity. See [Modality Selection](modality-selection.md).
- **Planifications** can enact that judgment in a particular run without redefining modality meaning or imposing a mandatory transition sequence.
- **Docs Standard** supplies possible structures to preserve material reasons and findings, when useful; it does not require documenting every transition.

Validating can produce new evidence or respond to feedback **when supplied**, informing Method's decision about the next modality. Validating is a Design phase, not a Method-owned modality-change phase. Ownership of Orientation remains unresolved.

## Historical source and migration choices

Primary source: [VSlices Method — Cambio de modalidad](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-switching.md).

Related:
- [VSlices Method — Selección de modalidad](https://github.com/vslices/docs/blob/main/es/products/method/patterns/modality-selection.md)
- [VSlices Design — Context-First](../design/modalities/context-first.md)
- [VSlices Design lifecycle](../design/lifecycle.md)

Preserved: six illustrative transitions, the changing-uncertainty trigger, risks of overextending each modality, observed change signals, minimal ceremony, proportional documentary continuity and the fact that change can reflect learning rather than failure.

Adapted explicitly: historical references to delivery feedback are interpreted under the approved Design lifecycle where **Validating** is the fifth phase. Received feedback is optional, and the decision to switch remains Method-owned rather than part of Design phase semantics.

Not established here: numerical switching thresholds, automatic routing, obligatory run restarts, fixed document templates, full canonical definitions of Problem-First or Slice-First, or Orientation ownership.

Historical public references to possible **Support Notes, Validation Notes, Decision Records, Context Documents, Use Case Documents and Process Documents** are examples of optional preservation mechanisms owned by Docs Standard, not mandatory artifacts of switching.
