# Foundations

## Status

Candidate shared foundations for VSlices.

Foundations exist to prevent several products from independently redefining concepts they all require in order to communicate coherently.

## Domain

`Domain` is the area of reality, knowledge, or activity about which a responsibility needs to understand, represent, support, or act.

It is not an architectural layer and does not mean the historical `VSlices.Domain` namespace.

## Domain Knowledge

`Domain Knowledge` is knowledge that an actor or system possesses, acquires, infers, or preserves about a domain.

## Domain Model

`Domain Model` is a selective and structured representation of Domain Knowledge built for a purpose.

```text
Domain
    -> knowledge about it

Domain Knowledge
    -> selective formalization

Domain Model
```

A Domain Model does not attempt to exhaust the domain.

## Other foundation candidates

The current candidate inventory includes:

- Semantics;
- Semantic Authority;
- Evidence;
- Continuity;
- Transformation;
- Realization;
- Materialization;
- Unknown / Underdetermination.

These names are not a closed taxonomy.

## Ownership under review

Two concepts that had previously been listed as suite-foundation candidates are deliberately **not promoted here yet**:

- Representability;
- Admissibility.

Current Framework evidence still treats meaning/representability and restrictions/admissibility as part of its conceptual semantic model.

Therefore the current question remains:

```text
suite foundation?
vs
Framework-owned semantic concept?
```

Until that question is resolved through evidence, the suite should not silently reassign their authority.

## Growth rule

A concept should live here when:

1. several products need it;
2. no single product should be able to redefine it unilaterally;
3. a shared definition reduces real ambiguity;
4. enough evidence exists to state at least a useful candidate meaning.

If a concept clearly belongs to Design, Method, Docs Standard, Framework, Tooling, or another product, this repository should record that ownership rather than duplicate the definition.
