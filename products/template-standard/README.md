# VSlices Template Standard

**Owner:** VSlices Template Standard. **Status:** bounded canonical conceptual definition based on the official specialized repository, 2026-10-09.

## Purpose

Template Standard owns **reusable knowledge for materializing and reconstructing semantic artifacts into human-facing representations**. It defines how a semantic state may be expressed in a specific medium while preserving sufficient evidence to reconstruct its meaning.

It does not define the source artifact's semantics, and it does not own the generic mechanism applying the template.

## Ownership boundary

- **Docs Standard** owns documentary kinds, stable question identities, question relationships and semantic constraints.
- **Template Standard** owns representation mappings, layout choices and reconstruction contracts for a specific materialization.
- **Tooling** owns the generic mechanisms for loading templates, rendering/materializing, reading/reconstructing, validating and supporting their lifecycle.
- **The authored artifact** is an editable realization and evidence; its visible syntax does not automatically redefine semantic authority.

This boundary is consistent with the Suite-level principle of grounded projections: a representation is a justified projection, not a competing definition.

## Semantic round-trip

For a human-editable representation, the current governing expectation is:

```text
semantic state
  -> materialize(template)
  -> editable representation
  -> read(template)
  -> semantically equivalent state
```

Byte-for-byte equality is not required. Representation-specific constructs (Markdown headings, table columns, lists, callouts, diagrams) are not themselves semantic question identities or semantic depth.

**Reconstruction must fail closed when semantic identity is ambiguous** rather than infer unsupported meaning from display text or accidental formatting.

## First supported witness

The official [vslices/template-standard](https://github.com/vslices/template-standard) currently registers only `markdown.question-tree` v0.1, a materialization of a Document question graph as hierarchical Markdown headings. The current implementation explicitly relies on structurally unique child identities where reconstructible, has instance markers for repeated answers, and does not assert support for arbitrary ambiguous branching.

The Context and Structure examples are **witnesses**, not a complete model of all documentary artifacts.

A future Domain Vocabulary presentation may map documentary questions to table columns instead of headings, demonstrating that semantic graph depth and display nesting need not coincide. This is **design pressure**, not a currently supported normative layout. Docs Standard must define the questions before Template Standard materializes them.

## Non-promoted possibilities

No general-purpose template language, arbitrary layouts, Support Note/Nexus/Continuity Path templates, template-version migrations or project-owned extension protocol is established by current source evidence. Their existence should be justified and tested before promotion.

## Relationship to Suite and official source

This Suite surface establishes the product identity and conceptual boundary; [vslices/template-standard](https://github.com/vslices/template-standard) is the official specialized source for deeper materialization contracts, manifest, YAML templates, examples and future extensions. Such extensions do not compete with the Suite's conceptual source of truth.

## Evidence

- [Official README](https://github.com/vslices/template-standard/blob/main/README.md)
- [Materialization model](https://github.com/vslices/template-standard/blob/main/docs/materialization-model.md)
- [Registered template](https://github.com/vslices/template-standard/blob/main/templates/markdown/question-tree.yaml)
- [Manifest](https://github.com/vslices/template-standard/blob/main/manifest.yaml)
