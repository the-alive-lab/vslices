# Product responsibilities

## Purpose

This surface declares product responsibility boundaries from the suite perspective.

It does not replace the internal definition each product owns.

## Independence

Products should preserve independent value within their responsibility.

VSlices Method is an intentional exception in one specific sense: part of its responsibility is composing and navigating other products and suite mechanisms during real work.

Tooling is not subordinate to Method.

## Design

Defines modalities and reasoning tools for approaching engineering problems.

Current modalities include:

- Context-First;
- Problem-First;
- Slice-First.

Design may use suite-level mechanisms such as Action Flow and Semantic Pressure without owning their base definition.

Candidate work forces currently have their strongest ownership affinity with Design.

## Method

Organizes how real work is navigated using the products and mechanisms that are useful in the current context.

Method may:

- select or switch Design modality;
- decide which continuity needs priority;
- apply suite mechanisms such as Semantic Pressure;
- decide when to deepen Action Flows;
- coordinate movement through the current lifecycle;
- incorporate feedback into the next iteration.

The current lifecycle has strongest affinity with Method, while its final ownership remains explicit rather than inferred from physical location.

## Docs Standard

Defines how documentary knowledge is preserved, related, composed, navigated, and represented.

Examples include:

- Documents;
- Nexus;
- Continuity Paths;
- documentary organizations;
- diagram realizations.

Docs Standard may realize suite mechanisms documentarily without thereby owning their base semantics.

The ownership of `Continuity Path` itself remains under explicit review. Existing evidence still places it in Docs Standard, so it must not be reassigned by assumption.

## Framework

Defines how sufficiently explicit knowledge may be represented and materialized as executable semantics and technological realizations.

Current Framework-owned or Framework-affine concepts include emerging surfaces such as:

- Space;
- Work;
- Grounding.

Current evidence also places representability and admissibility strongly inside the Framework conceptual model; suite-level promotion remains unresolved.

## Tooling

Makes supported capabilities operable, repeatable, and verifiable across products and mechanisms.

Tooling may support Docs Standard, Framework, or other suite surfaces when semantics are sufficiently defined.

Do **not** generalize this into “Tooling owns operational mechanisms”.

For current lowering work, the narrower established authority rule is:

```text
Tooling owns the rule language.
Rulesets own the rule vocabulary.
```

That means Tooling owns constrained mechanisms for expressing, validating, composing, and executing supported lowering knowledge, while revisable target vocabulary remains Ruleset-owned.

Automation does not acquire semantic authority merely by existing.

## Research / Alive Lab

Preserves observations, hypotheses, tensions, and evidence before promotion.

```text
observation
-> candidate
-> repeated evidence
-> stabilization
-> promotion
```

History and evidence remain distinguishable from the definition they support.
