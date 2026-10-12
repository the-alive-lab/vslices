# VSlices Intermediate Representation (VSIR)

**Conceptual owner:** VSlices Intermediate Representation  
**Status:** consolidated product responsibility (2026-10-11); the current VSIR 0.1 specification and its amendments remain experimental and should not be mistaken for a complete future language.

## Purpose

**VSlices Intermediate Representation defines reconstructible, versioned semantic representations of software concepts and their admissible relationships, independently of any particular source-code layout, tooling implementation, runtime or target programming language.**

Its responsibility is to answer **what an artifact asserts and under which language rules it can be interpreted and considered conforming**. It enables humans and AI agents to revisit semantic evidence without depending on an old chat or a particular lowerer. Concrete software realizations can witness a VSIR contract; a compiler, generated file or parser does not thereby acquire authority over that contract.

The [official specialized repository](https://github.com/vslices/intermediate-representation) defines the language grammar, file-level semantics and conformance expectations in depth. This Suite namespace states **product purpose, responsibility and cross-product boundaries**; it does not duplicate the full evolving specification.

## Language identity and semantic commitments

A complete, conforming VSIR document must explicitly identify:

```yaml
vsir: 0.1
kind: domain-type
name: StreetName
```

- `vsir`: which version of the semantic language interprets the file, **not** the represented software or target version.
- `kind`: which semantic artifact family is asserted.
- `name`: the artifact's semantic identity, independent of file or target-language identifier.

This is an **example of the current VSIR 0.1 artifact family**, not a prediction that every future VSIR file must be a Domain Type. During progressive authoring, a document may preserve fewer declarations and remain useful without being *conforming*.

The current [VSIR 0.1 specification](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION.md) is centered on `kind: domain-type` and contains source-level distinctions including:

- `shape: product | sum`, with named, distinguishable sum variants;
- semantic `state` versus observable `representation`, including shared and variant-local fields;
- `classification` and separately declared additional `traits`, plus obligations for identity, equality and maintained values;
- semantic type constructors such as `optional` and `sequence`, not target-library type strings;
- direct/derived state and explicit representation operations such as `represent`, `select`, `map` and `stringify`;
- `input` versus ordered `construction` steps, including `ensure`, `resolve`, `apply` and `refine`;
- compositional semantic expressions and locally scoped construction bindings under the experimental amendments.

These specifics describe **the present, limited language witness**, not universal Framework categories and not a promise that all forms are publicly authorable or lowerable in current tools. The main specification's `domain-type` family includes classifications such as `value-object`, `identifier`, `entity`, `maintained` and `aggregate-root`. Their current status in VSIR must not be confused with the evolving concepts in Framework.

## Governing language principles

1. **Semantic locality:** declarations and their semantic relations should remain together, rather than relying on unrelated files, implicit conventions or correlated names.
2. **Target independence:** represent semantic optionality, alternatives, state and transformation rather than `Option<T>`, C# helpers, SQL or other target-native syntax.
3. **No redundant assertion:** do not require repetitions of facts already implied by stronger language declarations; explicit authorship is preserved where it adds a real distinction.
4. **Explicit composition:** `Select(Represent(value), field)` and `Select(value, field)` are not presumed equivalent. A consumer must not insert `represent`, flatten a sum or discard variant identity just because a target projection is convenient.
5. **Fail closed:** malformed, unknown, contradictory or insufficiently authorized semantics must not be guessed or silently dropped. A missing target rule is a target-realization limit, **not** a reason to fabricate source meaning.
6. **Versioned reconstruction:** `vsir: 0.1` selects one intended language grammar and semantic interpretation; do not introduce shape-dependent legacy parsers with different meanings hidden under that same version.
7. **Evidence-led evolution:** discover additions through real artifacts, identify irreducible semantic pressure, revise language definitions and verify their executable support, preserving uncertainty and provenance.

## Three distinct questions of validity and support

The [authoring/lowering parity note](https://github.com/vslices/intermediate-representation/blob/main/AUTHORING-LOWERING-PARITY.md) is an **experimental design and evidence document**. It identifies three different questions:

| Question | Meaning | Primary responsibility |
| --- | --- | --- |
| **Progressive admissibility** | Can currently incomplete, reconstructible state safely continue the authoring process without inventing claims? | Authoring protocol and Tooling, under VSIR constraints |
| **VSIR conformance** | Does the complete artifact satisfy the language contract for its declared version/kind? | **Intermediate Representation** defines; conforming tooling checks |
| **Target lowerability** | Is there enough admitted semantics, target context, mechanism and Ruleset knowledge to realize it without invention? | Tooling + Ruleset + target environment |

These are **derived assessments**, not required lifecycle phases to store inside each `.vsir` file. In particular, **conforming does not mean authorable in the present CLI or lowerable to every target**.

Authoring and lowering traverse the **same semantic language** from different directions, not as mathematical inverses. Parity evidence should identify which layer lacks authoring, parsing, conformance, lowering or target mapping rather than weakening the authored language to mask a gap.

## Cross-product ownership

| Surface | Responsibility |
| --- | --- |
| **VSlices Intermediate Representation** | VSIR syntax, semantic language, versioning, reconstruction and conformance expectations |
| [VSlices Framework](../framework/glossary-reconciliation-2026-10-09.md) | Its own software semantics, capabilities, guarantees, executable models and realizations; may supply evidence for new VSIR expressiveness |
| [VSlices Tooling](../tooling/README.md) | Parsing, validation implementation, progressive authoring/discovery/update, search, transpilation, lowering and rebase mechanisms |
| [VSlices Ruleset](../ruleset/README.md) | Revisable target-specific realization vocabulary and deterministic lowering knowledge |
| [VSlices Template Standard](../template-standard/README.md) | Contracts for human-editable materializations and their reconstruction, not a competing VSIR grammar |
| [VSlices Protocols](../protocols/README.md) | Reusable traversal for reconstruction, migration and development; does not define what VSIR means |
| Consumer repository / project extensions | Grounded semantic claims and evidence about the actual software, plus explicitly authorized local extensions |

The planned rename `vslices/planifications → vslices/protocols` is **not yet a physical repository migration**. Older source references to Planifications retain their historical meaning.

The **Suite** is the canonical home for product purposes and boundaries. The **official IR repository** remains the detailed owning specification for language forms; the locations have complementary authority at different granularity.

## Specification maturity and official references

The specialized repository currently holds five documents:

- [`README.md`](https://github.com/vslices/intermediate-representation/blob/main/README.md): explicit language and repository authority.
- [`SPECIFICATION.md`](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION.md): **experimental normative VSIR 0.1** file grammar and semantics for the semantic-locality experiment.
- [`SPECIFICATION-REFINE-INTRINSIC.md`](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION-REFINE-INTRINSIC.md): **experimental normative companion** for ordered intrinsic refinement and named output bindings, present in `main` after [PR #1](https://github.com/vslices/intermediate-representation/pull/1). Not yet integrated into the main specification text.
- [`SPECIFICATION-CONDITION-EXPRESSIONS.md`](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION-CONDITION-EXPRESSIONS.md): **experimental normative companion** for expression-valued condition arguments and `concat-space` from the Name/FullName corpus.
- [`AUTHORING-LOWERING-PARITY.md`](https://github.com/vslices/intermediate-representation/blob/main/AUTHORING-LOWERING-PARITY.md): **experimental cross-repository note**, not an independent language definition.

Current executable coverage is described separately by [Tooling's capability evidence matrix](https://github.com/vslices/tooling/blob/main/docs/vsir-capability-matrix.md). The matrix is evidence of implementation support and gaps, not authority to amend VSIR semantics by accident.

## Open conceptual tensions — do not silently resolve

### 1. VSIR `domain-type` versus Framework evolution

Our [Framework review](../framework/glossary-reconciliation-2026-10-09.md) records **Domain Type as a retired Framework conceptual category**, whereas VSIR 0.1 currently defines `kind: domain-type` with a full family of obligations, classifications and traits; Tooling's current capability matrix also documents witnesses for that vocabulary.

**This is a live cross-product reconciliation question, not proof that an existing VSIR 0.1 artifact became invalid** or that old Framework semantics should be restored. Examine which relations are independently useful as VSIR semantic forms, which are historical Framework projections, and what genuinely changes language meaning. If incompatible meaning is introduced, provide an explicit, evidence-backed migration/version decision rather than silently reinterpret `vsir: 0.1`.

### 2. Intrinsic semantic contracts versus target Rulesets

The present [specification](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION.md) and [intrinsic-refinement amendment](https://github.com/vslices/intermediate-representation/blob/main/SPECIFICATION-REFINE-INTRINSIC.md) assign the active **Ruleset** not only target realization but also some intrinsic *semantic signatures, argument meanings and output names*. The current [Ruleset product boundary](../ruleset/README.md) instead emphasizes **target-lowering knowledge for already-admitted semantics**.

These formulations are in tension. An intrinsic call needs a justified target-independent meaning while the target realization remains replaceable. **Do not assume the location of that intrinsic contract is already resolved.** Investigate whether intrinsic semantic contracts belong to the versioned VSIR language, a separately authorized semantic vocabulary/extension, or a carefully distinguished non-target portion of Ruleset. Preserve currently implemented behavior as evidence while maintaining fail-closed conformance.

### 3. Grammar parity, artifact metadata and consumer evidence

The official Tooling [capability matrix](https://github.com/vslices/tooling/blob/main/docs/vsir-capability-matrix.md) records parser/conformance/lowering support that may exceed public `new/discovery/update` support, and nonsemantic `tags` handled at the artifact layer. Confirm gaps with current executable witnesses before treating supported tooling behavior as a normative VSIR guarantee. Additional VSIR kinds, broad extension semantics and mature version migration are **not** implied by this single initial corpus.

## Next responsible evolution

Use **real consumer case → semantic distinction and evidence → owning authority → minimal language change → Tooling/Ruleset realization → observable conformance/parity → revision**.

Avoid turning a convenient target behavior into VSIR semantics, treating every parser gap as a new language version, or equating the current Domain Type grammar with all future software representation.

**This review changes only the Suite-level definition.** It does not edit the VSIR specification, merge branches, renormalize existing `.vsir` files or claim a solved Framework/VSIR compatibility boundary.
