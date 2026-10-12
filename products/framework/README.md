# VSlices Framework

**Conceptual owner:** VSlices Framework.  
**Status:** emerging conceptual responsibility; active implementations and experiments do not exhaust the product.

## Purpose

Framework expresses and preserves **software-semantic intention** so that justified behavior can be composed, examined, validated, transformed and realized in executable forms. It distinguishes meanings and rules from specific technological realization mechanisms.

The canonical [public-glossary reconciliation](glossary-reconciliation-2026-10-09.md) is the current bounded source of reviewed Framework concepts, not an exhaustive stable ontology.

## Current conceptual orientation

- **Flow** remains in active investigation; absence from the `master` implementation is not conceptual retirement.
- **Feature** is a reusable definition for WorkFlows at Service level and WorkFlows or WorkProcesses at Product level. **WorkStep** is the relevant narrower work concept; their full contracts remain subject to evidence.
- **Capability** expresses a behavior or operation that may be requested or offered. **Guarantee** expresses a property a valid realization must satisfy in a specified scope. Availability of one does not prove the other.
- **Rules of Space** remain meaningful; the former **Domain Type** category is historical in Framework, and the formal status of `Invariant` is still to be verified.
- **Result / Error as Value** remain relevant. Trait, Effect and functional composition are generally implementation approaches, not obligatory universal Framework concepts.

Current .NET implementation experiments distinguish **Space, Work and Grounding**. Those are useful witnesses, not an automatic closed taxonomy of all future Framework semantics.

## Distinct responsibilities

- [Design](../design/README.md) defines how problems, requirements and candidate responses are understood and examined; Framework does not replace that methodology.
- [Intermediate Representation](../intermediate-representation/README.md) defines its **versioned** VSIR language and its conformance. VSIR 0.1 currently retains a `kind: domain-type` family: that contract is not silently invalidated or rewritten by Framework's evolving vocabulary.
- [Tooling](../tooling/README.md) implements authoring, validation and transformation mechanisms, but does not gain Framework conceptual authority by generating code.
- [Ruleset](../ruleset/README.md) supplies target-specific deterministic realization knowledge, without inventing missing semantic contracts.
- Concrete software [vslices/framework](https://github.com/vslices/framework) is the official specialized .NET realization and continuing experimental source; code, tests and branches witness what actually works.

For the unresolved VSIR/Framework and intrinsic-signature boundaries, see the [IR product review](../intermediate-representation/README.md#open-conceptual-tensions--do-not-silently-resolve).

## Next evidence

Consolidate Flow/Feature/WorkFlow/WorkProcess/WorkStep contracts against actual active implementation branches and consumer uses. Reconcile present Framework meanings with the versioned VSIR grammar **through explicit review and migration when warranted**, not through implicit parser changes or historical rewriting.
