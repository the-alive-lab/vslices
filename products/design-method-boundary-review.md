# Design / Method responsibility boundary — first migration review

Status: **candidate review**, not promoted product semantics.
Date: 2026-10-09.
Owner for this review: VSlices Suite product-boundary surface.

## Why this review exists

The current work on Software Development identified a practical distinction: the protocol needs to **use** an approach for understanding a client's problem and discovering justified requirements, while the **definition** of that approach belongs to VSlices Design. VSlices Method was described in this working discussion as concerning connections between two or more projects.

This is a **proposed clarification** of product responsibilities, not authority to retroactively rewrite the existing docs or product history.

## Evidence and precedence

1. [Current suite product responsibilities](README.md) (this directory) defines:
   - Design: modalities and reasoning tools for approaching engineering problems.
   - Method: navigation of work using products/mechanisms, modality selection, priority of continuity, lifecycle and feedback.
2. [Public Design projection](https://github.com/vslices/docs/blob/main/es/products/design/index.md) describes domain understanding, Context-/Problem-/Slice-First, heuristics and design reasoning independently of Framework.
3. [Public Method projection](https://github.com/vslices/docs/blob/main/es/products/method/index.md) describes coordinating Design/Docs Standard and preserving continuity across activities and iterations.
4. The active design discussion proposes:
   - Design as owner of working methodologies, including understanding a client's problem to **discover and justify** requirements rather than treating requested features as requirements by default;
   - Method as owner of the connection/coordination **between two or more projects**;
   - Planifications as owner of reusable protocols that **know when and how to invoke** methodologies without redefining them.
5. The candidate [Software Development meta-protocol](https://github.com/vslices/planifications/pull/3) already distinguishes understanding from architecture proposals but does not yet provide a complete source-owned methodology for customer problem discovery.

The public docs are evidence of previous and current communicated meanings; they are not the final tie-breaker over product-owned concepts. The active discussion has steering authority for this review, but cannot alone establish that all historical Method-owned mechanisms should be reassigned.

## First responsibility candidates

### VSlices Design

**Candidate responsibility:** Define and evolve methodologies, modalities, and reasoning instruments by which participants progressively understand problems and their context, discover and test justified requirements, explore alternatives, and examine design decisions.

The methodology does **not** automatically begin with requested features, assume software is necessary, or replace a customer's decision authority. A client statement is evidence to interpret, not automatically a confirmed requirement.

Potential included concepts: problem understanding, contextual investigation, requirements discovery and justification, modeling/option comparison, Context-/Problem-/Slice-First modalities, design forces and relevant criteria for changing approach.

Not automatically owned: executable protocol coordination, product-run state, documentary formal definitions, VSIR grammar or code implementation.

### VSlices Method

**Working proposal requiring validation:** Define how multiple projects relate, coordinate, preserve boundaries and maintain continuity between their distinct responsibilities or outputs.

This contrasts with the existing suite wording that assigns Method modality selection, lifecycle coordination, cross-product mechanisms and continuity of work within a project.

**Unresolved:** Does Method own both inter-project coordination and general navigation of work, or should those be separated across Design, Planifications and other owning surfaces? The fact that multiple VSlices products participate in a project does **not** by itself prove that Method's relevant unit is a project-to-project relationship.

Do not silently reassign lifecycle or Semantic Pressure simply to make the new wording consistent.

### VSlices Planifications

Reusable execution procedures and meta-protocols coordinate **use** of Design's methodologies, select bounded next efforts and preserve run continuity. They should link to Design-owned methodology rather than recreate its definition. A missing methodology is an owner finding, not license for the protocol to invent canonical Design.

### VSlices Docs

A public projection assembled from the definitions of suite and products. The public website does not become the owner because it currently contains the most elaborate explanation.

## Migration inventory — first pass

| Existing item | Present evidence | Candidate disposition | Need to examine |
| --- | --- | --- | --- |
| Design purpose and modalities | `vslices/docs/es/products/design/index.md` | Design-owned candidate, retain context | Product owner and detailed modality documents |
| Domain/problem understanding and requirements discovery | Active working distinction and Design's domain-understanding principle | Expand Design definition provisionally | Which methodology already exists and what counts as evidence/confirmation |
| Work modalities Context-/Problem-/Slice-First | Suite `products/README.md`; Design docs | Likely Design-owned | Method's historical modality-selection role |
| Method as work navigation and lifecycle/feedback | Suite `products/README.md`; public Method docs | **Conflict/open**; preserve until examined | Lifecycle location, Method/Design/Planifications responsibility |
| Method as relationship between 2+ projects | Current working definition | **Candidate**, not yet replacement | Meaning of project, coordination guarantees, existing relation mechanisms |
| Documentation and continuity artifacts | Docs Standard ownership already declared | Keep ownership | Integration versus semantic duplication |
| Protocol orchestration | Planifications | Keep procedural ownership | When the protocol invokes a Design methodology |
| Public docs `vslices/docs` | Existing projection | Update *after* authority settles | Link each page to owning source; avoid wholesale copy |

## How to proceed, incrementally

1. Inspect the detailed Design and Method docs and the suite's mechanisms/lifecycle/relationships; index claims with current owner, candidate owner, evidence and conflicts.
2. Test the narrower Method definition against real cases: single-project iterative delivery; multi-project coordination; multi-product Suite orchestration. Avoid equating products with projects.
3. Formulate a small product-owned definition for Design and for Method **only once** the responsibility tension is resolved. Record any historical meaning being narrowed or transferred.
4. Identify documentary and protocol dependencies that must link to new authorities. Treat `vslices/docs` as the projection to update **after** promotion.
5. Migrate one bounded concept at a time with source trace, redirects/links as appropriate, and semantic checks; do not bulk move publication content into the suite.

## What this review does not decide

- Whether Design and Method each require separate future repositories under `the-alive-lab`.
- Whether lifecycle and modality selection should move ownership from Method.
- Whether requirements discovery is a new named methodology or part of an existing Design model.
- Whether the Software Development meta-protocol needs a new child procedure.
- Whether all projects' truth sources must physically reside in a single repository; **authority is based on responsibility rather than storage location**.

## Next pressure

Resolve the current Method definition's broad work-navigation responsibility against the newer proposed inter-project boundary, using the detailed existing materials and concrete counterexamples, before editing product normative definitions or public projections.

## Clarification of "projects" — 2026-10-09

The human author of the working distinction clarified that **"Method connects two or more projects" referred to the projects/products comprising VSlices itself** (e.g. Method with Design, Method with Framework), **not** to independent client software projects. The preceding "inter-project" interpretation was a misunderstanding in the review, not an original restriction on Method.

The intended candidate boundary is therefore:

- **Design** defines methodologies and reasoning techniques for understanding problems, discovering and justifying requirements, and designing responses.
- **Method** coordinates how the different VSlices product responsibilities connect and participate in a resolution; coordinating several surfaces does not transfer ownership of their meanings to Method.
- **Planifications** defines reusable procedures that operationalize those interactions in a concrete run, referring to the owners rather than redefining them.

One software project can call upon several VSlices products. Method's applicability does not depend on there being two separate client projects. The number "two or more" is explanatory, not a required runtime cardinality or a limitation to pairwise connections.

**Effect on earlier interpretation:** the supposed contradiction between Method's inter-client-project exclusivity and its existing cross-Suite navigation **dissolves**. The previous H1/H3 discussion remains recorded as evidence of the misreading, not as an equally current expression of the human intent. This clarification supports the broad coordination role already stated in `products/README.md` and the Method ownership of Semantic Pressure; neither requires reassignment on that basis.

**Still open:** precise meaning and boundary of "coordination" versus Design methodology and Planifications orchestration; ownership of lifecycle stage definitions versus selection/navigation of stages versus concrete run execution; modality definition versus modality selection; whether some concepts need a more specific owning product. Do not imply this clarification settles those issues.

**Revised next pressure:** map concrete Method–Design, Method–Docs Standard and Method–Framework relationships, labeling what Method coordinates and what the other product defines, then examine the lifecycle and modalities against those examples before any normative migration or public docs update.
