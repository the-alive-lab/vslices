# Cross-product consistency review — PR #2

**Review date:** 2026-10-11  
**Reviewed branch:** `review/design-method-responsibility-boundary` in [the-alive-lab/vslices](https://github.com/the-alive-lab/vslices/pull/2).  
**Status:** bounded cross-product documentation and authority review. This is **not** a semantic conformance test, deployment approval, or assertion that all specialized products have finished evolving.

## Objective and method

Examine the current Suite definition as one coherent source rather than independently validating each product file. Test the following claims:

1. Product definitions, Method/Design relations, and a shared mechanism cannot silently assert conflicting ownership.
2. The **current** Design lifecycle and Method Orientation must be distinguishable from their historical evolution and from still-unmigrated operational protocols.
3. The central Suite source must coexist with explicitly recognized official **detailed, versioned product specifications** without treating implementation code or public docs as automatic authority.
4. Cross-product references must resolve; historical sources should be identified without promoting outdated names, modalities, phases or requirements.
5. Material unresolved tensions must be declared rather than papered over to make the PR look complete.

Inspected all **47 Markdown files** on the current branch, including historical/bootstrap files, across product definitions, mechanisms, lifecycle, foundations, relationships and promotion. Compared with the official current repositories for [VSIR](https://github.com/vslices/intermediate-representation), [Tooling](https://github.com/vslices/tooling), [Ruleset](https://github.com/vslices/ruleset), [Template Standard](https://github.com/vslices/template-standard), [Framework](https://github.com/vslices/framework), [Docs Standard](https://github.com/vslices/docs-standard), [Protocols (currently Planifications)](https://github.com/vslices/planifications) and [historical public documentation](https://github.com/vslices/docs). Existing PR maturity was also checked where it affects claims.

## Confirmed contradictions and corrections

| Finding | Evidence of inconsistency | Action within PR #2 |
| --- | --- | --- |
| **R-01: Orientation ownership** | [Design/Method product source](README.md) and [Method Orientation](method/orientation.md) declare Method ownership, while Suite root, [lifecycle](../lifecycle/README.md) and the [open-ownership ledger](../relationships/open-ownership-questions.md) still said *owner unresolved*. | Aligned **current** statements: Method owns situated actor/team Orientation; operational triggers and reconciliation remain open. Historical `Orientation → ... → Feedback` is preserved as an antecedent, not current lifecycle. |
| **R-02: Semantic Pressure owner** | [Mechanism source](../mechanisms/semantic-pressure.md) assigns Method ownership; [relationship map](../relationships/README.md) incorrectly assigned ownership to Suite. | Fixed `owned-by → Method`; kept cross-product applicability and its candidate relationship schema distinct. |
| **R-03: Completed modality migrations described as incomplete** | [Modality Selection](method/modality-selection.md), [Modality Switching](method/modality-switching.md), [Context-First](design/modalities/context-first.md) and [Problem-First](design/modalities/problem-first.md) retained now-obsolete claims about Problem-First, Slice-First, Modality Switching or Orientation. | Updated live references to the existing [Design modality sources](design/README.md) and Method Orientation. Kept older phase semantics as labeled history. |
| **R-04: Incorrect current repository identity** | Root and product sources contained `the-alive-lab/vslices-suite`; current canonical repository is `the-alive-lab/vslices`. | Corrected current host/path examples in [root](../README.md), [Design](design/README.md) and [Docs Standard](docs-standard/README.md). Historical/bootstrap mention remains intentionally preserved in [bootstrap history](../bootstrap/README.md). |
| **R-05: Conceptual vs official specification authority** | The root's instruction to treat other repositories as implementation evidence could be read as demoting actual normative sources, e.g. VSIR 0.1 and Docs Standard definitions. | Added **authority by granularity** to [root](../README.md): Suite is canonical for product meaning/boundaries; expressly recognized official repositories may own detailed, versioned normative contracts, without silently redefining the Suite or older contract versions. |
| **R-06: Missing product entrypoints** | Method and Framework had their material definitions dispersed in the inventory and other documents, unlike the remaining product namespaces. | Added minimal [Method](method/README.md) and [Framework](framework/README.md) entrypoints that route to current owning definitions, research and realizations without reproducing their specifications. |
| **R-07: Research mistaken for product inventory** | [Product inventory](README.md) ended with `Research / Alive Lab` under product headings. | Made explicit that research evidence and Alive Lab relations do **not** automatically constitute additional VSlices products or transfer actor ownership. |
| **R-08: Historical assessments read as current decision state** | [Initial Design/Method review](design-method-boundary-review.md) and [assessment](design-method-boundary-assessment.md) preserved open ownership questions that subsequent discussion resolved. | Appended 2026-10-11 reconciliation checkpoints. Earlier judgments and mistakes remain visible as dated evidence, not equally current statements. |

No technical implementation, frozen research evidence, protocol run or official versioned VSIR grammar was rewritten by this review.

## Explicitly unresolved cross-product tensions

### U-01 — Framework `Domain Type` vs VSIR 0.1 `kind: domain-type`

The [Framework reconciliation](framework/glossary-reconciliation-2026-10-09.md) treats **Domain Type** as a retired Framework category. The [official VSIR 0.1 specification](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION.md), by contrast, still normatively defines a `domain-type` artifact family and classifies variants such as `entity`, `value-object`, `identifier` and `aggregate-root`.

This is a real conceptual divergence, **not proof that a previously conforming VSIR 0.1 artifact is now invalid**. Investigate which semantics are independent of Framework's implementation evolution and which truly require an explicit VSIR language migration/version. **Do not** rebrand an old artifact or silently relax the parser to achieve cosmetic agreement.

### U-02 — Intrinsic semantic contracts vs Ruleset ownership

Current [VSIR specification](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION.md) and [refinement amendment](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION-REFINE-INTRINSIC.md) assign intrinsic argument/output **semantic signatures** to an active Ruleset. The [Ruleset product](ruleset/README.md) currently defines Ruleset mainly as **target-specific realization vocabulary for already-admitted source semantics**.

The open question is who owns the target-independent meaning of an intrinsic and how that interacts with versioned VSIR semantics, authorized extension vocabulary, Ruleset contracts and executable validation. This review does **not** resolve it. No renderer is authorized to infer meaning from its own existence.

### U-03 — Adoption of approved lifecycle by operational and public projections

The conceptual source now distinguishes the **Design-owned five phases** including `Validating` and **Method-owned Orientation**. The existing [shared VSlices Usage protocol](https://github.com/vslices/planifications/blob/main/protocols/vslices-usage/README.md) and portions of [Software Migration](https://github.com/vslices/planifications/blob/main/protocols/software-migration/README.md) still preserve the earlier **Feedback**-based operational traversal. The [Software Development candidate](https://github.com/vslices/planifications/pull/3) applies the new distinctions but remains an open candidate PR.

Adapt these owning projections in separate, reviewable work; do not rewrite their historical executions or claim this Suite PR changed them.

### U-04 — Product and procedure evolution still pending

The planned `vslices/planifications → vslices/protocols` **repository rename has not been executed**. Protocol-owned supervision/run conventions are candidate material. Continuity Path ownership remains a recorded [question](../relationships/open-ownership-questions.md), with current Docs Standard authority preserved. Work-forces ownership also remains candidate. Those are not merge blockers simply because they are unresolved; their maturity and authority must remain transparent.

## Reference and validation results

- **47 Markdown files inspected**, including bootstrap historical material.
- **150 local Markdown file-path links checked against the branch tree: 0 missing targets.**
- Sampled/checked **27 links to `vslices/docs`** and **40 source-file links to official specialized repository trees**: no missing target among those checked. These are path checks, not a proof that every external section anchor or URL will remain valid forever.
- The three local anchor targets requiring explicit attention (`#suite-principle--grounded-projection` twice and `#open-conceptual-tensions--do-not-silently-resolve`) match present heading wording.
- **No GitHub Actions runs were returned for the reviewed PR branch** at this check. This is a documentation/authority review; **no build, runtime, cross-product VSIR parser or lowering tests were executed**.
- Existing issue/PR review submissions and inline threads were checked; no submitted reviews or threads were returned at this cut.

## Merge assessment and next work

**Assessment: conceptually mergeable as an explicitly bounded Suite source consolidation, not as a certification of complete semantic interoperability.** The previously silent current-source conflicts found in this review are corrected. The remaining U-01/U-02 semantic tensions, and the separate protocol/public adoption work U-03/U-04, are explicitly described and should not be silently closed merely to merge this documentation PR.

Before treating downstream consumers as aligned, independently verify VSIR/Framework and intrinsic ownership against real artifacts and executable tests, and migrate the older operational/public projections through their owning repositories. A future contrary witness should revise the responsible concept with provenance rather than preserve this report's conclusions by fiat.

**No merge is performed by this review.**
