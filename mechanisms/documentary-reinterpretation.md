# Documentary Reinterpretation — candidate mechanism

**Status:** candidate; not a validated algorithm or a new mandatory Docs Standard artifact. **Scope:** evidence interpretation for one standalone work iteration; wider applicability remains open.

## Purpose

When new documentary evidence appears, **classify and interpret it as Orientation Factors**, then consider its relationships to previously documented evidence. An interpretation may find no current impact on effort. A subsequent item can make an earlier interpretation more precise, change it, or leave it justified.

A **material change or nuance in an Orientation Factor classification, together with its reasons**, produces **interpretive impact**. The pair of relevant evidence and incoming impact is conveyed along explicit documentary relationships declared in the **front matter**, **not topical tags**. Each related receiving document reinterprets that pair in its own context, potentially generating a further justified impact and continuing propagation. If no material outgoing impact arises, that local branch stops.

## Candidate cycle

```text
new evidence with provenance and explicit front-matter relationships
  -> classify and interpret: Semantic / Technical / Delivery / Resource
  -> identify factor change or nuance, with reasons (or no material change)
  -> first interpretive impact, if material
  -> traverse explicit related documents
  -> each recipient reinterprets {evidence, incoming impact}
  -> produce its own resulting factor change/nuance + reasons, if material
  -> propagate that updated impact along its own documentary relationships
  -> end branch if no material outgoing impact
```

Interpretations are not facts. Preserve evidence identity and provenance separately from revisions of its interpretation. What is received is **not a fixed impact strength**; its significance can grow, diminish, change type, or become immaterial in each document's context. Accumulated impacts might reinforce or counteract one another, but **no numeric impact algebra is defined**.

An unchanged classification may carry additional reasoning. Whether that difference is material enough to propagate must be examined; do not blindly propagate unchanged messages. Absence of present impact does **not** mean permanent irrelevance.

## Documentary and authority boundaries

- **Docs Standard** owns actual documentary identities, front-matter relationship properties and preservation semantics. This proposal uses those relationships **without inventing their key names, directionality, closure, or an all-relations-traversable rule**. Verify the exact current contracts before implementation.
- **Tags** can classify or help discover topics, but do **not** constitute this propagation's traversal edges.
- **Orientation Factors** describes the revisable factor classifications associated with evidence; it is not the propagation transport or an automatic modality selector.
- **Value Orientations** consumes the resulting interpreted factors to reconsider response affinity and modality recommendation. Propagation need not move the triangle.
- **Method** retains selection authority; **Tooling or an LLM** may implement or suggest interpretations without silently replacing documentary and organizational authority.

## Open behavior and performance questions

Document relations may differ in kind, direction and relevance. Propagation through any specific relation needs its contract and a justified receiving interpretation. Multiple paths to the same document, cycles, duplicate evidence, repeated updates, impact composition and convergence require explicit handling before large-scale execution. Do not demand all documents be reprocessed in parallel or invent a universal scheduler prematurely.

The relevant optimization question is how to produce a correct bounded result under resource limits while preserving provenance and revisability. A small new evidence item can legitimately lead to extensive downstream reinterpretation, but the **number of affected documents is not itself evidence of correctness**.

This concept originated from the VSlices Orientation Factors and Value Orientations exploration on 2026-10-12. It has not been experimentally validated or promoted to a generic universal interpretation engine.
