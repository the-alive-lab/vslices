# VSlices Framework

**Conceptual owner:** VSlices Framework.  
**Status:** emerging conceptual responsibility; active implementations and experiments do not exhaust the product.

## Purpose

Framework expresses and preserves **software-semantic intention** so that justified behavior can be composed, examined, validated, transformed and realized in executable forms. It distinguishes meanings and rules from specific technological realization mechanisms.

The [public-glossary reconciliation](glossary-reconciliation-2026-10-09.md) preserves an earlier bounded review, **not the exhaustive or most recent conceptual state**. Consult the approved conceptual articulations in [Language Specification](https://github.com/vslices/lang-specification/tree/main/concepts) alongside Framework's own responsibility. Conceptual ownership of Framework is not transferred to the language repository.

## Framework organizational surfaces

The current organizational model distinguishes four Framework-owned surfaces: [Spaces](spaces.md) defines spaces of domain concepts; [Work](work.md) defines functionalities and required access/exposure capabilities; [Grounding](grounding.md) supplies mechanisms to realize those capabilities; [Hosting](hosting.md) assembles configured realizations to make a participant available. These are responsibilities, not aliases of DDD layers. Terminology for exposure forms (e.g. Endpoint, TimedTask) and their provider contracts remains under review. Hosting of a participant must not be confused with operational **Composition** of multiple products and services.

## Current conceptual orientation (reconciled with Language Specification)

The approved articulations [C-021 Spaces](https://github.com/vslices/lang-specification/blob/main/concepts/C-021-spaces.md), [C-005 Work](https://github.com/vslices/lang-specification/blob/main/concepts/C-005-work.md), [C-006 Grounding](https://github.com/vslices/lang-specification/blob/main/concepts/C-006-grounding.md) and [C-020 Feature](https://github.com/vslices/lang-specification/blob/main/concepts/C-020-feature.md) articulate **Spaces, Work and Grounding** (which now sit alongside Hosting in the Framework organizational orientation), without declaring an exhaustive taxonomy or requiring physical project separation. **Spaces** (organizational surface) is distinct from a **Space** (semantic concept whose admissible instances are Points); **Work** organizes Features and their required Capabilities; **Grounding** organizes concrete realizations for the required capabilities and execution conditions. These are **not** aliases of Domain, Application and Infrastructure from DDD. A Feature does not necessarily require external effects or Grounding.

The current language-generation research does not automatically revise earlier VSIR 0.1 normative contracts. Conceptual definitions and grammar/conformance remain distinct authorities. The following glossary distinctions are retained as historical context where not superseded:

- **Flow** remains in active investigation; absence from the `master` implementation is not conceptual retirement.
- **Feature** is an identifiable semantic unit of functional behavior with input, output and result promise ([C-020](https://github.com/vslices/lang-specification/blob/main/concepts/C-020-feature.md)). Earlier statements about WorkFlow, WorkProcess and WorkStep are historical orientation; their detailed contracts remain subject to evidence.
- **Capability** expresses a behavior or operation that may be requested or offered. **Guarantee** expresses a property a valid realization must satisfy in a specified scope. Availability of one does not prove the other.
- **Rules of Space** remain meaningful; the former **Domain Type** category is historical in Framework, and the formal status of `Invariant` is still to be verified.
- **Result / Error as Value** remain relevant. Trait, Effect and functional composition are generally implementation approaches, not obligatory universal Framework concepts.

**Ownership clarification pending:** VSlices Framework is understood as a software development system that **uses Language Specification**. Spaces, Work and Grounding belong conceptually to **Framework**; their articulation in the language repository is not a transfer of ownership. The precise distinction between Framework's organizational concepts and their expression in Language Specification is **pending explicit review in the Language Specification discussion**. Do not silently resolve it here, revise those approved concept files, or treat their location as authority. The .NET implementation remains evidence of a realization, not a closed taxonomy.

## Distinct responsibilities

- [Design](../design/README.md) defines how problems, requirements and candidate responses are understood and examined; Framework does not replace that methodology.
- [Language Specification](../lang-specification/README.md) owns **versioned** VSIR language contracts, conformance and exploration of the new language generation; historical VSIR 0.1 remains a separate versioned contract. VSIR 0.1 currently retains a `kind: domain-type` family: that contract is not silently invalidated or rewritten by Framework's evolving vocabulary.
- [Tooling](../tooling/README.md) implements authoring, validation and transformation mechanisms, but does not gain Framework conceptual authority by generating code.
- [Ruleset](../ruleset/README.md) supplies target-specific deterministic realization knowledge, without inventing missing semantic contracts.
- Concrete software [vslices/framework](https://github.com/vslices/framework) is the official specialized .NET realization and continuing experimental source; code, tests and branches witness what actually works.

For the unresolved VSIR/Framework and intrinsic-signature boundaries, see the [Language Specification product orientation](../lang-specification/README.md).

## Next evidence

Consolidate Flow/Feature/WorkFlow/WorkProcess/WorkStep contracts against actual active implementation branches and consumer uses. Reconcile present Framework meanings with the versioned VSIR grammar **through explicit review and migration when warranted**, not through implicit parser changes or historical rewriting.
