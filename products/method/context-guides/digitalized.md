# Digitalized work — Context Guide

**Owner:** VSlices Method. **Status:** migrated context guidance.

## Situation and principal risk

Software already represents part of the organization's work, perhaps through UIs, APIs, reports, automation or integrations. It may embody real rules **and** obsolete decisions, accidental constraints and tolerated workarounds.

**Risk:** treating the existing implementation as authoritative domain truth, or discarding its accumulated evidence merely because it appears imperfect.

## Method guidance

Distinguish:
1. How real work currently happens.
2. How current software represents it.
3. How people have adapted around the software.

Recover enough continuity among those perspectives and current decisions to support the next responsible change; do **not** reverse-engineer or document the entire system by default.

When context and intent are unknown, **Context-First** may help; when a particular behavior is painful but its cause is uncertain, **Problem-First** may help; when a bounded safe change can produce meaningful evidence, **Slice-First** may help. Method chooses contextually, rather than inferring the modality from software's mere existence.

Historical guidance associates Business Scenario, Domain Context, Software Project, Customer Product and Consumable Service Continuity Paths with different aspects of the current change. The needed path depends on the **continuity at risk**; Method coordinates their use but does not own Docs Standard's definitions.

The implementation must be treated as a source of evidence and constraints, not copied as the desired future by default. Validating can reveal whether a change improves actual work, and respond to feedback if received.

## Provenance

[Original Method guide — Digitalized scenario](https://github.com/vslices/docs/blob/main/es/products/method/context-guides/scenarios/digitalized-scenario.md). Public observation tables and optional documentary examples remain source evidence, not a mandatory all-system audit.
