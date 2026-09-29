# VSlices Suite

This repository is the canonical working surface for definitions whose semantic authority belongs to **VSlices as a suite**, and for explicit relationships between suite-level semantics and product-owned semantics.

It is not the public documentation site and it does not replace the repositories of VSlices products.

## Responsibility

This repository may:

- define shared foundations;
- define mechanisms whose identity belongs to VSlices across products;
- declare product responsibility boundaries;
- preserve cross-product relationships;
- record candidate lifecycle or design models that affect more than one product while their ownership is still being validated;
- preserve promotion history and unresolved authority questions.

It must not:

- absorb semantics that clearly belong to one product;
- duplicate a product definition merely to centralize files;
- turn a current realization into a universal definition;
- promote a useful hypothesis to stable semantics only because it now has a name.

## Authority rule

```text
suite-owned semantics
    -> defined here

product-specific semantics
    -> defined by the owning product

research / uncertain ownership
    -> preserved as candidate evidence or an explicit ownership question
```

A product may use, document, realize, specialize, render, validate, or operationalize a VSlices mechanism without thereby becoming the authority that defines its base semantics.

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

Reusable VSlices mechanisms whose semantic identity remains recognizable across multiple products or realizations.

Current candidates:

- [Action Flow](mechanisms/action-flow.md)
- [Semantic Pressure](mechanisms/semantic-pressure.md)

### Lifecycle

Current candidate model for how VSlices work enters, advances through, leaves, and re-enters an iteration.

Its strongest current ownership affinity is Method, but that ownership is still recorded explicitly rather than assumed from repository location.

### Forces

Candidate groups of forces that bias the direction and cost of engineering effort.

Their strongest current ownership affinity is Design.

### Products

Suite-level responsibility boundaries between Design, Method, Docs Standard, Framework, Tooling, Research, and other products.

### Relationships

How definitions are owned, used, realized, preserved, rendered, operationalized, supported, or challenged.

### Promotion

How ideas move from observation to canonical knowledge without rewriting their history.

### Bootstrap

Historical evidence that led to this surface, including the original internal-knowledge proposal and the project-context source snapshots preserved before this repository became canonical.

See [`bootstrap/`](bootstrap/README.md).

Bootstrap material is evidence, not current authority.

## Public documentation

Public documentation is a deliberate projection of canonical knowledge.

```text
suite definitions + product definitions
        ↓
public projection
        ↓
vslices/docs
        ↓
MkDocs / Read the Docs
```

The public navigation may optimize learning and onboarding without becoming the accidental ontology of VSlices.

## Reconstruction rule

When reconstructing VSlices:

1. use this repository for suite-level meaning and cross-product authority;
2. use the owning product repository for product-specific semantics;
3. use Research / Alive Lab and historical artifacts as evidence for how a definition emerged;
4. use `vslices/docs` as a public projection, not as the primary authority merely because it is published.
