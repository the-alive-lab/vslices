# VSlices Suite

This repository is the **canonical source of truth for the VSlices Suite and all of its products** (Method, Design, Docs Standard, Framework, Tooling, and others). It preserves foundational meanings from which distinct downstream projections can be developed.

It defines suite-wide and product-specific concepts, product identities and responsibilities, processes, intentions and normative constraints when appropriate. This does not mean that every concept must become a prescriptive specification, or that every possible projection must be represented here.

It is **not** the public documentation website, implementation repository, or necessarily the place where each downstream realization is authored.

## Responsibility

This repository may:

- define shared foundations;
- define mechanisms whose identity belongs to VSlices across products;
- define product purposes, responsibilities, concepts and processes, as well as their boundaries;
- preserve cross-product relationships;
- record candidate lifecycle or design models that affect more than one product while their ownership is still being validated;
- preserve promotion history and unresolved authority questions.

It must not:

- erase the internal ownership of a product merely because its source is hosted here;
- duplicate the same definition across suite and product paths;
- turn a current realization into a universal definition;
- promote a useful hypothesis to stable semantics only because it now has a name.

## Authority rule

```text
suite-wide semantics
    -> defined here, with suite-level ownership

product-specific semantics
    -> defined here, within that product's conceptual namespace

research / uncertain ownership
    -> preserved as candidate evidence or an explicit ownership question
```

A product may use, document, realize, specialize, render, validate, or operationalize a VSlices mechanism without thereby becoming the authority that defines its base semantics.

**Centralized canonical hosting does not collapse product responsibility.** Design, Method, Tooling, etc. retain distinct conceptual ownership even though their definitions live in one repository.

Likewise, physical location does not establish semantic authority.

## Maturity

Definitions should make maturity explicit.

Useful states include:

- `candidate`;
- `emerging`;
- `active`;
- `stable`;
- `superseded`.

These labels are descriptive working states, not a universal schema yet.

## Current structure

```text
vslices-suite/
├── foundations/
├── mechanisms/
├── lifecycle/
├── forces/
├── products/
├── relationships/
├── promotion/
└── bootstrap/
```

### Foundations

Shared concepts needed by several products without independent redefinition.

### Mechanisms

Reusable VSlices mechanisms and explicit cross-product mechanism relationships.

A mechanism being applicable across several products does not by itself make the suite its conceptual owner. Ownership and applicability must be recorded separately.

Current candidates:

- [Action Flow](mechanisms/action-flow.md)
- [Semantic Pressure](mechanisms/semantic-pressure.md) — Method-owned, suite-wide applicability
- [Path of Least Resistance](mechanisms/path-of-least-resistance.md)
- [Path of Most Continuity](mechanisms/path-of-most-continuity.md)
- [Path of Most Value](mechanisms/path-of-most-value.md)

### Lifecycle

The approved five-phase iterative lifecycle is now **Design-owned**, in [products/design/lifecycle.md](products/design/lifecycle.md). The Suite lifecycle surface preserves cross-product context and historical transitions, not competing phase authority. Orientation ownership remains open.

### Forces

Candidate groups of forces that bias the direction and cost of engineering effort.

Their strongest current ownership affinity is Design.

### Products

Canonical product definitions and their responsibility boundaries, including [VSlices Design](products/design/README.md). Product-specific meanings are defined here under their owning product's namespace; independent realization repositories are projections rather than competing sources of truth.

### Relationships

How definitions are owned, used, realized, preserved, rendered, operationalized, supported, or challenged.

### Promotion

How ideas move from observation to canonical knowledge without rewriting their history.

### Bootstrap

Historical evidence that led to this surface, including the original internal-knowledge proposal and the project-context source snapshots preserved before this repository became canonical.

See [`bootstrap/`](bootstrap/README.md).

Bootstrap material is evidence, not current authority.

## Definition, intention, specification and projection

The canonical repository is the **source** for concepts, products, processes and other elements that can justify a downstream projection. Several useful categories may overlap:

- **Definition**: establishes what a concept, responsibility, product or process means.
- **Intention**: establishes what outcome a realization seeks and why.
- **Specification**: makes constraints or obligations of a realization examinable.
- **Projection**: interprets, expresses or materializes selected canonical meanings and intentions in a specific context.

These are distinctions of responsibility, **not** a mandatory four-document format or linear pipeline. "Specification" is not a synonym for everything canonical: explanatory concepts, goals and open questions can be important sources without being implementation contracts.

Examples:

- **Tooling's canonical definition** describes capabilities and constraints it should provide. Tooling implementation is a technical realization/projection, and its implementation details do not automatically redefine the source.
- **Public documentation** projects VSlices concepts with a pedagogical intention, and a web implementation additionally realizes that intention in pages, navigation and interaction.
- **TDidacta** may contribute pedagogical methodologies, design and examination of that intention without gaining authority to redefine VSlices concepts. Whether pedagogical intent is itself canonical to a particular publication or a separate governed artifact depends on the responsibility in question; no automatic transfer of ownership is implied.

```text
the-alive-lab/vslices-suite
  concepts + products + processes + intentions + constraints
       |                            |
       +--> Tooling realization     +--> pedagogical projection
                                           |
                                           +--> web publication (vslices/docs)
```

The branches are illustrative, not exhaustive and not invariably sequential. Sources and projections should retain links to the meanings and intentions that justify them. New evidence from a realization may **challenge** a source, but does not silently overwrite its authority.

## Suite principle — grounded projection

**Artifacts and realizations should emerge as justified projections of understood problems, needs and requirements, through the continuity preserved about them.**

User stories, screens, APIs, database tables, implementation tasks, models, documents and executable behavior are not merely different names for requirements or problems. They are potential **projections** of progressively understood meaning, decisions and constraints, in forms appropriate to their own responsibilities.

This is a **Suite-wide** expectation, not a constraint owned by Design alone:

- **Understanding and continuity** make the source problem, relevant requirements, uncertainty, evidence and intention reconstructible.
- **Design** explores and justifies responses, without presuming that a requested artifact or software feature is already warranted.
- **Method** coordinates how participating product responsibilities contribute and how their context remains situated.
- **Docs Standard** can preserve the distinctions and their relations without mandating a document for each projection.
- **Framework and Tooling** may express or realize selected semantics in executable or operational forms without inheriting authority to redefine their origin.

A projection is **not a mechanical copy**. It can specialize or transform meaning and can reveal new constraints or evidence. Such evidence may justify revising prior understanding and requirements; it must not silently change their authority or erase the reason a projection exists.

The principle does **not** require that every low-level artifact have a separate written trace, that every result be software, or that every observed request become a validated requirement. It asks that **material choices remain explainable from the problems and requirements they address**, at the level of continuity appropriate to their consequences.

### Projection surfaces beyond VSlices products

A projection is not restricted to a Suite product's implementation or to published documentation. **Surreal Atlas** and potential work-management applications (including systems analogous in function to Jira) may provide different **surfaces of projection** over grounded problems, requirements, decisions and their continuity.

Examples of possible views include semantic maps and navigable relationships, work items and assignment states, pedagogical explanations, and operational representations. These are **illustrative possibilities**, not claims that a specific integration or shared storage model already exists.

A projection surface may record new observations, assignments or work-state changes within its own authority. Such facts can become evidence informing the underlying understanding; they do not automatically redefine the problem, requirement or intention projected.

**Conceptual authority, representation, storage and operational ownership must not be conflated.** The principle does not demand a universal central database, a prescribed bidirectional synchronization mechanism, or identical schemas across surfaces. Each concrete implementation must establish how it preserves provenance and avoids competing meanings when appropriate.

### Decision lineage

The earlier Design framing warned against confusing user stories, screens, APIs, tables and implementation tasks with problems or requirements. The Suite-wide reformulation strengthens this from a prohibition against confusion to a **positive relationship of grounded projection**, shared across products. Design retains its methodology of understanding and justification, but does not own the general principle.

## Public documentation

`vslices/docs` is a **didactic and web projection** of canonical VSlices meanings, not the authority establishing those meanings. Its pedagogical intent and its website realization are distinguishable even when housed in the same project.

## Reconstruction rule

1. Look to **this repository** for canonical meanings of the Suite **and each VSlices product**.
2. Use implementation and publication repositories as evidence of existing realizations, constraints and feedback, **not** as automatic authority to change the underlying definition.
3. Use Research and historical artifacts to reconstruct emergence, test claims and flag unresolved ownership questions.
4. Record substantive revision of canonical sources explicitly; propagate the results to relevant projections rather than silently rewriting history.
