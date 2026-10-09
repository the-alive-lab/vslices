# Method boundary — evidence and counterexample assessment

Status: **analysis / unresolved**. Date: 2026-10-09. Companion to [Design/Method first review](design-method-boundary-review.md).

## Sources inspected

- [Suite product responsibilities](README.md) (current, on branch): Method coordinates traversal of products, modalities, continuity, feedback.
- [Suite lifecycle](../lifecycle/README.md): lifecycle is a candidate, currently Method-affine, but no final ownership established.
- [Semantic Pressure](../mechanisms/semantic-pressure.md): explicitly Method-owned, applicable across the Suite. It distinguishes second-order interrogation governance (where/why/how far/when to stop) from concrete interrogation techniques that can belong to Design.
- [Suite relationships](../relationships/README.md): definition/usage/realization are separate relations; an owner is not automatically the party that applies a concept.
- [Public Method](https://github.com/vslices/docs/blob/main/es/products/method/index.md), [Patterns](https://github.com/vslices/docs/blob/main/es/products/method/patterns/index.md), [Context Guides](https://github.com/vslices/docs/blob/main/es/products/method/context-guides/index.md): selection and coordination of working approaches within a project, continuity across activities and collaboration.
- [Public Design iteration](https://github.com/vslices/docs/blob/main/es/products/design/iteration-flow/stage-intro.md): attributes the earlier iterative cycle explicitly to Design. This conflicts with the Suite's present Method affinity, and predates explicit Feedback and Orientation refresh.
- Working conversation: proposed Design as owner of methodologies for understanding client problems and discovering requirements; Method as connecting two or more projects; Planifications as coordinating execution of methods without defining them.

## Competing interpretations (not promoted)

**H1 — inter-project-only Method.** Method relates at least two projects; within-project methodologies and iteration live in Design, while Planifications operates them. Advantage: crisp project-level boundary. Problem: it fails to account for Method's existing second-order Semantic Pressure, single-project context guides, and modality/continuity orchestration unless those definitions are reassigned.

**H2 — second-order Method.** Method governs relationships and coordination among **distinct responsibilities / surfaces / continuities**, which may occur inside one project or between projects; Design owns the concrete techniques for understanding and shaping a problem. Advantage: preserves Semantic Pressure's documented scope and current suite coordination. Problem: may overlap with Planifications unless conceptual selection/governance is distinguished from concrete protocol execution; diverges from a literal “two or more projects” criterion.

**H3 — split existing Method responsibilities.** Narrow Method to inter-project relations; migrate modality/lifecycle to Design or Planifications, and review Semantic Pressure separately. Advantage: literal compatibility with proposed boundary. Problem: significant semantic relocation, risk of making protocol implementation owner of methodological meaning, and substantial historical/projection repair without demonstrated benefit.

None is confirmed by the current evidence alone.

## Counterexamples and boundary tests

| Case | Required behavior | H1 (inter-project only) | H2 (second-order) | Ownership implication |
|---|---|---|---|---|
| One team developing one software product | Decide when to apply problem-oriented inquiry, change modality, preserve intent across building | Method arguably absent despite existing Method guides explicitly supporting such work | Method may coordinate Design / Docs / Feedback within one project | Project count alone is an insufficient explanation of current Method documents |
| Customer request “build feature X” | Investigate underlying work before treating X as a validated requirement | Design methodology can own the investigative technique | Same; Method may determine when to invoke/stop/revisit the technique | Strong Design ownership of technique; no necessary cross-project dependency |
| Two projects exchange domain responsibility or evidence | Define handoff, authority and continuity across separate projects | Method squarely relevant | Method squarely relevant | Supports inter-project Method responsibility; does not prove exclusivity |
| Multiple VSlices products are used in one repository | Select Design/Docs/Tooling according to current pressure | Requires reallocation of existing Method role | Naturally within second-order coordination | “Product” of the Suite is not equal to independent “software project” |
| Semantic Pressure interrogates a single claim during a one-project run | Decide what distinction merits another question and when to stop | Currently Method-owned mechanism becomes unexplained | Fits second-order pressure on a continuity, even in one project | Existing canonical mechanism directly challenges exclusivity of H1 |
| Software Migration and Software Development both need start/state/feedback | Reuse compatible operational procedures, without losing domain specificity | Common Planifications mechanisms possible | Also possible | Shared occurrence does not transfer conceptual authority to Method |

## Assessment

The **methodology versus application** boundary is presently well supported: Design can own concrete client-problem understanding and requirements-discovery techniques; Planifications can invoke and coordinate their use without defining them. Research specifications are evidence, not canonical Design by default.

The **inter-project-only Method** boundary is **not yet supported as an exclusive replacement**. Current canonical Semantic Pressure and Suite product definitions provide concrete counterexamples to its exclusivity. This does not disprove the intended inter-project responsibility; it shows that making it the *entire* Method boundary would entail deliberate semantic migration or a refinement of what “projects”/“connections” means.

The **lifecycle** has *conflicted attribution*: public Design calls the earlier iteration a Design flow, Suite labels revised iteration Method-affine but explicitly candidate, Planifications operates the traversal. Do not treat either file's location as final ownership evidence. Separate (a) definition of the stages, (b) when to use or revisit them, and (c) execution/run-state operation before choosing owner.

## Recommended next bounded investigation

Reconstruct the provenance of Method and Design definitions around Semantic Pressure, modality selection and lifecycle, then ask one discriminating question for the boundary: **Does Method coordinate only independently owned projects, or more generally independently owned responsibilities/continuities (including within a project)?** Test it against an actual one-project development run and an inter-project handoff.

Do **not** rewrite `products/README.md`, `lifecycle/README.md`, `mechanisms/semantic-pressure.md` or `vslices/docs` in this step. The migration inventory should mark Method's exclusive scope as unresolved; first-order Design techniques and Planifications invocation remain useful provisional separations.

## Immediate implementation consequence

Software Development may *use* a Design-owned problem-understanding methodology when one is sufficiently defined, while currently preserving missing methodology as an explicit gap. It must not manufacture Design authority merely by documenting a startup questionnaire. Conversely, the absence of a settled Method ownership boundary does not prevent continued bounded implementation under Planifications.
