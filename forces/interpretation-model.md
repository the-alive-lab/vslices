# Work Forces — evidence interpretation model (candidate)

**Status:** exploratory semantic specification, not a validated inference algorithm.  
**Scope:** the situation of one standalone group iteration, feeding Method Orientation and modality selection.  
**Conceptual relationship:** [Work Forces](README.md) interpret available evidence and may change [Value Orientations](../mechanisms/value-orientations.md). They are not the same as orientations.

## Problem

Neither uncertainty labels nor pressure words are enough to choose a modality. The same observation can imply different responses depending on who knows what, whether that knowledge is available, what the organization needs, which restrictions matter, and how the evidence relates to other observations.

The intended mechanism is not `document -> triangle movement`; it is **`evidence -> justified Work Force interpretation -> viable response affinity -> triangle position`**. The interpretation must remain open to correction.

## Interpretive dimensions

These are **questions about real evidence**, not an obligatory form or numerical taxonomy.

| Dimension | What must be distinguished | Candidate implications |
| --- | --- | --- |
| **Semantic / epistemic** | Local knowledge versus general organizational knowledge; organization versus developing group; uncertainty, contradictory understanding, missing experts or trustworthy sources | Determines whether broad contextual inquiry is viable, what can be understood locally, and risks of unsupported generalization |
| **Technical** | Existing systems, couplings, critical invariants, available interfaces and observed limitations | May make local realization safe or dangerous; may justify more focused problem investigation or contextual work |
| **Delivery** | Actual need, urgency, observable deadlines, opportunity window and acceptable feedback cycle | Can favor short-term business value, but urgency alone never proves that Problem-First or Slice-First is appropriate |
| **Resource** | Availability of people, time, money, infrastructure and capacity to access needed expertise | Changes what investigation or implementation can actually be sustained; can alter effort and possible response |

**Organizational needs** and **operating context** provide evidence interpreted within and across these forces. A deadline is not knowledge about processes. A client's statement about a process is not automatically proof that the developing group understands it. Interpretations may overlap rather than belonging to exactly one category.

## Minimal reasoning contract — per relevant evidence item

1. **Observation and provenance:** what was actually observed, when, and from whom or which artifact; distinguish a report, a direct observation and a later inference.
2. **Knowledge boundary:** what area and actor/group does the claim concern? Local, general or not determinable? Which sources or experts can substantiate it?
3. **Force interpretation:** what semantic/technical/delivery/resource pressure or enabling condition is indicated; why does the evidence support this and what would challenge it?
4. **Response implications:** which of Context-First, Problem-First and Slice-First become more/less defensible or viable? State the mechanism, including missing expertise or inability to bound implementation.
5. **Orientation implication:** how might relative Most Value, Most Continuity and Least Resistance emphases change **for the process**, not according to eventual benefits?
6. **Counterinterpretation and limits:** what alternative reading remains compatible, and what further evidence would distinguish the alternatives?

If the evidence does not discriminate, leave the inference indeterminate. No predetermined pressure-to-vertex vectors, mandatory numbers or keyword-to-modality rules are authorized.

## Examples (hypothetical, not research findings)

**Example A — local expertise but no broad process expert.** Evidence: several team members can describe and validate their local tasks, while no credible source can reconstruct the cross-area workflow. Semantic uncertainty is high *generally*, lower *locally*; source availability makes broad Context-First difficult or nonviable now. If one task can be safely bounded and tested, a Least Resistance / Slice-First affinity is defensible. Without a safe boundary, no modality should be automatically selected.

**Example B — process experts available, missing traceability.** Evidence: domain experts can explain cross-area workflows, while relationships between organizational processes and current software are not reconstructible. Semantic Work Forces support the feasibility of Context-First to establish process/software continuity. Most Continuity may become more prominent even though the organization already knows its own work.

**Example C — short-term deadline and identified business pain.** Evidence: a business operation has a visible problem and a real upcoming deadline. Delivery and resource forces may favor Most Value / Problem-First if investigating the concrete problem is viable. If the cause is already sufficiently known and a small safe realization is possible, Slice-First remains a rival; the deadline alone cannot choose.

## Position vs evidence quantity

A candidate triangle midpoint may mean either (1) weakly discriminating evidence or (2) materially supported competing responses. Show **position** independently of **evidence quantity**. As a deliberately minimal experimental indicator, count traceable evidence items considered, distinguishing duplicates and irrelevance; never describe the count alone as calibrated confidence. A high count can still be biased, contradictory or low quality.

Docs Standard can preserve the evidence, interpretation, differences from earlier interpretation and reasons for a change. This proposal does not introduce a new compulsory document type or impose a universal schema.

## Minimal test before prescribing a mapping

Take two or more independently documented standalone cases with comparable surface features but different viable responses. For each case, reconstruct the interpretation **without using the observed modality as an input**. Then ask whether the forces and source availability distinguish the defensible orientation/modality and whether a rival interpretation can explain the same evidence. Compare against existing uncertainty-only modality guidance. Document failures and unresolved ambiguity rather than optimizing the model to fit the known answer.

This note refines the current model for inspection **before** VS-STU-021 findings; it does not report that the study was executed. Method remains responsible for an actual selection judgment; Design owns modality semantics.
