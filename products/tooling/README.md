# VSlices Tooling

**Semantic owner:** VSlices Tooling. **Status:** bounded product-level consolidation based on the current specialized repository (2026-10-09).

## Purpose

Tooling makes semantically defined capabilities and transformations **operable, repeatable, inspectable and verifiable** across the VSlices ecosystem. It creates mechanisms to author, inspect, validate, transform, materialize and maintain projections, preserving the authority and uncertainty of their sources.

Tooling is **not** defined by one CLI, one target platform, or a claim of ownership over all operational mechanisms. Its [official specialized source](https://github.com/vslices/tooling) supplies concrete mechanisms and evolving executable specifications.

## Responsibility boundaries

| Surface | Authority |
| --- | --- |
| [VSlices Suite](../../README.md) | Shared conceptual principles and cross-product boundaries |
| [Docs Standard](../docs-standard/README.md) | Documentary semantic identities, questions and relations |
| [Template Standard](../template-standard/README.md) | Layout and reconstruction contracts for specific representations |
| [Intermediate Representation](https://github.com/vslices/intermediate-representation) | VSIR language semantics |
| **Tooling** | Generic operations for progressive authoring, inspection, validation, transformation, projection, rebase and lifecycle |
| [Ruleset](https://github.com/vslices/ruleset) | Revisable target vocabulary and realization knowledge |
| Consumer project / extensions | Concrete evidence, local configuration and explicitly admitted project-owned extensions |
| Target-native ecosystem | Target facts owned by the platform, e.g. .NET build/compiler facilities |

**A tool performing an operation does not thereby acquire authority over the meaning of that operation.**

The specific lowering boundary recognized in the current implementation is:

> Tooling owns the **constrained rule language**; Rulesets own the **target vocabulary expressed through that language**.

This is not a license to generalize that Tooling owns every operational mechanism.

## Working mechanisms

### Progressive semantic authoring

A progressively specified artifact can expose currently available decisions and value grammars through **discovery**. A client can then request explicit **updates** without reproducing the full grammar or inventing missing semantic assertions. The current specialized implementation supports a `new → discovery → update → discovery` loop.

Keep these independent:

- **Progressively valid:** can participate in incremental reconstruction.
- **Conforming:** its asserted semantics satisfy the applicable language and validation environment.
- **Publicly authorable:** exposed through present guided authoring operations.
- **Lowerable:** has enough semantic, target and project knowledge for a supported projection.

Failure at one of these boundaries does not automatically establish failure at all others.

### Semantic conservation

Tooling must preserve semantic structure that a supported transformation recognizes; unknown or malformed semantic assertions must remain visible as explicit failures, not silently disappear. An implementation may complete **target implementation details** but must not invent **missing source semantics**.

A missing deterministic target rule is a reason to stop or report insufficiency, not permission to derive semantics from a convenient generated file.

### Projection and reconstruction

Tooling may materialize artifacts according to the owning Template Standard's representation/reconstruction contract, or lower semantic intermediate representations using explicitly authorized target knowledge. Layout and target syntax do not determine the source semantic identity.

For human-maintained generated realizations, operational lineage and rebase can preserve separate deterministic ancestry and human changes; lineage is evidence for reconstruction, **not** independent semantic authority.

### Extensions and uncertainty

Locally admitted semantic extensions, installed Ruleset snapshots and operating configuration are distinct. Installing or updating Rulesets must not silently replace project-owned semantic extensions. The presence of a renderer does not authorize semantic validity.

Tooling must distinguish **unknown / unsupported / incomplete / contradicted** wherever those distinctions affect decisions. Lack of an implemented lowering path must not be misreported as semantic invalidity.

## Current official realization (evidence, not the product's exhaustive definition)

The [official Tooling repository](https://github.com/vslices/tooling) currently includes the `vslices` CLI and operations for project initialization, progressive VSIR creation/discovery/update/search, transpilation, lowering, rebase, Ruleset management and self-update. Its C#/.NET adapters and CLI command layout are **implementation surfaces**, not a universal Tooling ontology.

Its VSIR parser/validator code lives alongside Tooling for implementation reasons; **VSIR language authority remains with Intermediate Representation**. Current authoring coverage is narrower than some parser/conformance/lowering support, and experimental capability matrices describe evidence rather than universal future promises.

## What this definition does not promote

- An exhaustive list of CLI commands or mandatory command names.
- C#/.NET-specific lowering and project layout as universal Tooling semantics.
- VSIR syntax, traits, classes or language grammar as Tooling-owned meanings.
- Installed Ruleset vocabulary as built-in unchangeable Tooling semantics.
- The historically described Docs Standard L0/L1 documentation templates as current authority.
- An unrestricted plugin ecosystem or template language inferred from limited extension experiments.

## Official sources and provenance

- [README and current boundaries](https://github.com/vslices/tooling/blob/main/README.md)
- [Agent instructions](https://github.com/vslices/tooling/blob/main/AGENTS.md)
- [Semantic authoring affordances](https://github.com/vslices/tooling/blob/main/docs/semantic-authoring-affordances.md)
- [VSIR capability evidence matrix](https://github.com/vslices/tooling/blob/main/docs/vsir-capability-matrix.md)
- [Ruleset boundaries](https://github.com/vslices/tooling/blob/main/docs/rulesets.md)
- [Historical product decision](https://github.com/vslices/tooling/blob/main/docs/decisions/0001.vslices-tooling-definition.md)

The historical decision established Tooling as an independent product, initially motivated by documentary generation. Subsequent evidence expanded its mechanisms substantially without collapsing Docs Standard, Template Standard, Ruleset or VSIR authority into Tooling.
