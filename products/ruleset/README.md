# VSlices Ruleset

**Semantic owner:** VSlices Ruleset. **Maturity:** bounded conceptual definition based on the official experimental repository (2026-10-09).

## Purpose

Ruleset owns **revisable, source-owned knowledge for deterministically realizing already-admitted semantics in specific technological targets**. It allows target mappings to evolve independently of the executable mechanisms that interpret them.

It does not define what source concepts mean, whether a new semantic construct is valid, or how authoring and orchestration must work. The [official Ruleset repository](https://github.com/vslices/ruleset) is the specialized source of target vocabularies, distributable manifests, mappings and experiments.

## Authority boundary

- **VSlices Intermediate Representation:** source language meaning and recognized semantic structures.
- **VSlices Tooling:** constrained rule language, parsing/validation/authoring mechanisms, loading, invocation and lowering orchestration.
- **VSlices Ruleset:** target-specific vocabulary and deterministic realization knowledge expressible through that rule language.
- **Consumer project:** its specific semantic evidence, configuration and explicitly admitted extensions.
- **Target ecosystem:** native technological meaning and runtime/compiler behavior.

**Tooling owns the constrained rule language. Rulesets own the target vocabulary expressed through that language.** A rule may specify how an admitted operation is realized, not silently establish that a source operation exists or what it means.

## Operational consequences

1. **Semantic admission precedes target realization.** A matching renderer does not validate unknown VSIR semantics.
2. **Missing target knowledge is an explicit limit.** No lowerer may invent an interpretation because a matching mapping is absent.
3. **Target specialization does not redefine the source.** For example, a projection expressed as an explicit composition of `represent` and `select` must not be collapsed to direct `select` without evidence of equivalence.
4. **Revisability and reproducibility coexist.** Projects may install a source-owned snapshot for deterministic offline use; replacement/update belongs to that snapshot's lifecycle.
5. **Consumer-owned extensions stay separate.** The project's semantic-extension overlay is not part of the source-owned Ruleset snapshot and must survive its replacement.
6. **Grow from evidence.** New rule-execution primitives and target mappings should answer observed representational pressure, not anticipate a universal plugin ecosystem.

## Current specialized witness

The official repository currently contains a `vslices-ruleset` 0.1 manifest and C# catalogs for target types, intrinsic expressions and related deterministic mappings. Experiments with `normalize`, optional representations and projections reinforce the boundary between VSIR semantics, Tooling mechanisms, Ruleset mappings and project extensions.

These concrete manifests, placeholder bindings, C# expression templates and currently admitted targets **belong to the specialized realization**. They are not a universal Ruleset grammar or requirement that every VSlices project use C#.

## Not promoted

- A renderer as authority to invent missing VSIR semantics.
- An unrestricted plugin, dependency or package ecosystem.
- Project-owned extension catalogs inside a replaceable Ruleset distribution.
- A fixed technology target list, complete lowering vocabulary, or guaranteed multi-target parity.
- The current Ruleset manifest or exact placeholder regex as Suite-wide meaning.

## Provenance and official references

- [Ruleset README](https://github.com/vslices/ruleset/blob/main/README.md)
- [Manifest](https://github.com/vslices/ruleset/blob/main/manifest.yaml)
- [Normalize/extension authority experiment](https://github.com/vslices/ruleset/blob/main/experiments/normalize-ruleset-boundary/README.md)
- [TicketTrayFilter projection experiment](https://github.com/vslices/ruleset/blob/main/experiments/ticket-tray-filter-projection-relation/README.md)

This Suite namespace defines product meaning and points to the official source for deeper specialized implementations; neither layer should duplicate the other's responsibility.
