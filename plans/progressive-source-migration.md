# Progressive source migration

Status: experimental baseline, updated from the Ticket Support / Identities reconstruction experiments.

This plan describes a progressive migration/reconstruction process for taking an existing codebase, identifying and organizing its concepts, expressing justified semantics in VSIR, and producing executable witnesses without requiring whole-system understanding up front.

The plan is intentionally iterative and evidence-driven. It should evolve when real migrations expose a better sequence, a missing feedback loop, or an assumption that does not survive contact with source evidence.

For the current cross-repository model:

- [`vslices/intermediate-representation`](https://github.com/vslices/intermediate-representation) owns VSIR language semantics;
- [`vslices/tooling`](https://github.com/vslices/tooling) owns executable authoring/discovery/validation/lowering mechanisms;
- [`vslices/ruleset`](https://github.com/vslices/ruleset) owns target-specific deterministic realization knowledge;
- the [VSlices protocols repository](https://github.com/vslices/protocols) owns migration/reconstruction traversal and protocol coordination; this plan is maintained in the VSlices suite repository.

## Objective

Given:

```text
original codebase + surrounding evidence
migration/reconstruction objective
coherent target scope
```

produce an increasingly justified semantic model and executable implementation while preserving uncertainty.

The core traversal remains:

```text
observe
  -> name
  -> associate
  -> reorganize
  -> detail
  -> lower
  -> observe again
```

The modern Tooling interaction refines the detailing step into:

```text
new
  -> discovery
  -> update
  -> discovery
  -> ...
  -> lower
  -> observe
```

The commands assist traversal; they do not own epistemic decisions.

## 1. Analyze original evidence

Inspect source code and its surrounding evidence, including when relevant:

```text
source files
existing tests
runtime behavior
configuration
persistence schema
API contracts
UI behavior
documentation
migration notes
human narrative
```

The goal is not to explain the whole system. It is to identify concepts, relationships, behaviors and uncertainties relevant to the current objective.

Do not force implementation structures directly into VSIR. First ask what semantic fact the implementation appears to witness.

## 2. Name concepts before forcing semantics

As soon as a concept can be recognized, give it a stable semantic name even if little else is known.

A progressive artifact may begin as:

```yaml
vsir: 0.1
name: StreetName
```

and may carry provisional tags when useful:

```yaml
tags: [addressing, street]
```

Tags organize investigation; they are not semantic classifications.

At this stage it may be sufficient to know:

```text
this concept exists
this is a useful semantic name
it appears associated with these other concepts
```

If `kind` or another semantic fact is already justified, establish it. Do not invent facts merely to make the artifact look complete.

## 3. Consolidate and reorganize progressively

Repeat analysis and naming until the source is no longer being explored as an undifferentiated mass of files, classes and functions.

Use tags, observed relationships and investigation outcomes to reorganize the concept corpus.

Reorganization may affect:

```text
folder/location
working clusters
investigation order
candidate boundaries
which concepts are inspected together
```

It must not silently create semantic facts.

A coherent scope exists when the concepts relevant to one useful portion of the migration objective are organized well enough to refine without obviously severing required relationships.

## 4. Detail semantics through state-driven authoring

Once a concept has enough evidence to refine, use the VSIR language and Tooling authoring protocol progressively:

```text
vslices new vsir <Concept>
vslices discovery vsir <Concept>
vslices update vsir <Concept> ...
vslices discovery vsir <Concept>
```

The governing rule is:

> Advance only from evidence actually available. Preserve uncertainty instead of filling semantic gaps by intuition.

`discovery` exposes the semantic decisions currently available from the artifact's present state. `update` applies one or more justified decisions atomically.

Do not populate every available section at once. Iterate:

```text
inspect evidence
  -> discover current semantic affordances
  -> choose one justified decision
  -> inspect advertised value grammar if structured
  -> update
  -> validate
  -> discover again
  -> return to source evidence
```

This is a state-driven semantic reconstruction loop, not a static form-filling exercise.

## 5. Grammar-driven discovery

When a semantic decision accepts a structured value, Tooling may advertise the grammar needed to express that value.

This matters because an agent should not need an embedded copy of the complete VSIR authoring grammar.

Conceptually:

```text
artifact affordance
  -> what semantic assertion can be established now

value grammar affordance
  -> which semantic forms can express its value
```

For example, a representation mapping may expose expression forms such as `represent`, `select`, `map`, or `stringify`, including nested value kinds.

Grammar discovery tells the agent what forms are valid. It does not decide which form represents reality.

## 6. Preserve explicit evidence over convention

Conventions may reduce authoring or lowering burden, but they must not override stronger authored evidence.

Reusable rule discovered through `Location`:

> Explicit semantic evidence outranks a convenience convention.

For example, an explicit construction relation establishing a state coordinate through `apply` + binding + `refine` takes precedence over a same-name input convention.

This rule applies beyond that concrete case: where direct authored semantics and naming/layout convention conflict, the explicit semantic relation wins unless the language contract says otherwise.

## 7. Lower coherent concepts early enough to learn

When one or more concepts are semantically coherent enough for the objective, lower them:

```text
vslices lower ...
```

Do not wait for every concept in the migration to be complete.

Lowering serves two purposes:

```text
materialization
  -> produces target implementation from current semantics

evidence
  -> reveals missing semantics, missing target knowledge, incorrect assumptions or integration constraints
```

Compilation, tests and runtime behavior are observations about the current reconstruction. They are not permission for the lowerer to invent missing domain semantics.

## 8. Treat authoring and lowering as two traversals of one language

The current experiments establish a stronger architecture:

```text
partial knowledge
  -> new / discovery / update
  -> VSIR
  -> lower
  -> target witness
```

Authoring and lowering are not mathematical inverses, but they should operate over the same VSIR semantic language from opposite directions.

This leads to the **authoring parity** criterion.

A VSIR construction is fully supported when:

```text
discovery can explain how to express it
new/update can author it
validation can check it
lower can consume it
Ruleset can materialize it when target realization is required
```

When one side understands a semantic construction and the other cannot express/consume it, the gap is evidence for the next experiment.

## 9. Use real artifacts as parity witnesses

Do not generalize from invented examples when the consumer corpus can exercise the mechanism.

For each increasingly complex real VSIR artifact:

```text
reconstruct through new -> discovery -> update
validate
lower the exact normalized artifact
compile/test/observe target witness
record asymmetries
```

The `Location` experiment is the current strongest witness because it combines:

```text
structured semantic types
derived state
representation composition
transform input
resolve
nested apply
mapped/container apply
refine
```

The next artifacts should extend coverage rather than introduce a new interaction protocol unless real evidence requires one.

## 10. The two main learning loops

### Discovery and organization loop

```text
analyze source
  -> name concepts
  -> tag associations
  -> consolidate
  -> reorganize
  -> analyze again
```

Output: an organized corpus of named concepts, not necessarily completed semantics.

### Semantic reconstruction and materialization loop

```text
inspect evidence
  -> discovery
  -> update semantic model
  -> validate
  -> lower coherent concepts
  -> observe executable witness
  -> return findings to evidence/semantics
```

Output: increasingly justified semantic artifacts and executable witnesses.

The loops are nested and allow backward movement at any time.

## 11. AI traversal protocol

An AI agent should carry plan state rather than treat the process as a one-way checklist.

For each working iteration, preserve at least:

```text
migration objective
current coherent scope
source evidence inspected
new/changed concepts
current tags/associations
semantic facts added or changed
current discovery frontier used
structured grammar forms relied upon
uncertainties/hypotheses
reorganizations performed
concepts ready for lowering
lowering/build/test observations
authoring/lowering parity gaps
next source evidence to inspect
```

Decision procedure:

```text
if important concepts remain unnamed
  -> analysis + naming

if concepts exist but relationships/boundaries are unclear
  -> consolidate + reorganize

if coherent concepts have shallow semantics
  -> source inspection + discovery + update

if discovery exposes a structured value
  -> follow advertised grammar; do not invent syntax

if concepts can produce a useful witness
  -> lower

if lowering exposes semantic uncertainty
  -> return to evidence + semantic detailing

if lower consumes something authoring cannot express
  -> close authoring parity gap

if authoring expresses something lower cannot consume
  -> close lowering parity gap

if new evidence exposes missing concepts
  -> return to naming/tagging even late in migration
```

## 12. Resource-aware agent planning and escalation

Migration planning should not assume that every AI-assisted operation requires the strongest available model, nor that increasing model capacity is the correct response to every failure.

When evidence from repeatable benchmarks exists, record the **minimum viable capability** for each class of operation. For quantized local models this may include a `minimum_viable_quantization`, but the concept is broader than quantization: it identifies the least expensive execution capability that remains acceptably reliable for the operation under its actual constraints.

Example planning knowledge:

```yaml
operation_profiles:
  source-fact-extraction:
    minimum_viable_quantization: IQ1_M
    preferred_quantization: Q2_K

  discovery-selection:
    minimum_viable_quantization: Q2_K
    preferred_quantization: Q3_K_M

  semantic-mapping:
    minimum_viable_quantization: Q4_K_M
    preferred_quantization: Q5_K_M
```

These values are empirical and environment-dependent. They must come from observed performance under representative prompts, context providers, Tooling affordances and validation mechanisms rather than from model size alone.

### Quantization is also a resource-planning variable

Quantization affects more than isolated answer quality. Lower-bit weight representations usually reduce the memory footprint of model weights and the amount of memory traffic required during inference. On constrained CPU systems this can affect whether the model remains resident in physical RAM, how much context can be retained, whether multiple workers can coexist, and whether paging destroys throughput.

The relevant runtime footprint is not only model weights:

```text
model weights
+ KV cache
+ tokenizer / model metadata
+ temporary inference buffers
+ runtime overhead
+ operating-system and application memory
```

Reducing weight precision therefore does not imply an equal proportional reduction in total process memory. In particular, KV-cache cost is substantially influenced by context length and runtime/cache representation rather than by the quantization of model weights alone.

For planning, treat at least these variables independently:

```text
quantization / effective bits per weight
model weight footprint
configured context length
KV-cache footprint
peak working set
available physical RAM
pagefile / swap pressure
prompt-evaluation throughput
output-generation throughput
CPU utilization and effective frequency
power / thermal state
parallel worker count
```

A quantization that is slightly weaker in semantic quality may still be operationally superior if it avoids paging, leaves enough RAM for development tools, permits a larger useful context, or enables multiple constrained workers to run concurrently.

Conversely, a higher-precision quantization may be justified for an operation whose semantic ambiguity requires it even when it reduces parallelism.

This means migration benchmarks should measure resource behavior alongside quality. Useful observations include:

```text
peak RAM / working set
available RAM before, during and after inference
pagefile or swap usage
model load duration
prompt-evaluation tokens/second
output-generation tokens/second
context length
CPU utilization
CPU frequency / throttling when observable
power-source state when relevant
wall-clock duration
output-token count
```

Where practical, compare resource efficiency using derived measurements rather than tokens/second alone. Candidate measures include:

```text
useful semantic work / GB-hour
accepted semantic decisions / GB-hour
human-hours saved / GB-hour of compute
human-hours saved / human supervision hour
```

These are exploratory planning metrics until repeated migrations establish which correlate with real outcomes.

Resource planning should also account for **parallel composition**. One large worker is not automatically preferable to several smaller workers. For example, multiple low-bit workers may independently extract source facts, inspect data flow or classify deterministic evidence while a stronger worker is reserved for ambiguous semantic mapping or arbitration.

A planner may then combine:

```text
operation profile
available RAM / CPU / GPU
model and KV-cache footprint
parallelism
wall-clock budget
energy budget
risk tolerance
available context providers
Tooling constraints
escalation routes
```

and choose an execution plan that minimizes resource cost while preserving required reliability.

This can favor several smaller workers over one permanently expensive worker. Parallel workers may own narrow operations such as source-fact extraction, data-flow observation, discovery inspection or structured classification, while a stronger local agent handles ambiguous semantic mapping.

Conceptually:

```text
cheap constrained worker(s)
  -> structured evidence / candidate decision
  -> validation or disagreement detection
  -> stronger local worker only when needed
```

Do not conflate **capability escalation** with **authority escalation**.

A local agent may fail because of insufficient reasoning capacity, but it may also encounter insufficient context, conflicting evidence, a Tooling gap, a semantic ambiguity with no justified resolution, or a decision whose authority belongs elsewhere. Increasing quantization/model capability does not resolve all of those cases.

Escalations should therefore carry a reason, for example:

```text
insufficient-capability
insufficient-context
semantic-ambiguity
tooling-gap
authority-required
conflicting-evidence
repeated-failure
```

Possible routing:

```text
insufficient-capability
  -> stronger local model

insufficient-context
  -> context provider / compiler analysis / repository evidence

semantic-ambiguity
  -> stronger interpretive actor or VSlices Development

tooling-gap
  -> VSlices Development / Tooling evolution

authority-required
  -> the human or organization that owns the decision

repeated-failure
  -> stronger external/frontier actor, Development, or human review
```

A frontier model or VSlices Development can therefore be an escalation target through an API or supervised handoff rather than a permanently active dependency. Human escalation remains appropriate when authority, consequences or missing domain knowledge require it.

This suggests two related planning measurements:

```text
minimum_viable_quantization
  -> least local quantization observed to execute an operation reliably

minimum_viable_actor
  -> least capable/authoritative actor class that can legitimately resolve it
```

The second cannot always be reduced to model capability. A stronger model may understand a decision without having authority to make it.

A resource-constrained migration plan should prefer:

```text
smallest demonstrated viable capability
  -> resource-compatible execution
  -> deterministic validation / Tooling feedback
  -> explicit escalation on uncertainty or failure
```

rather than assigning the strongest available actor to every operation.

Benchmark results may therefore feed planning as:

```text
benchmark evidence
  -> operation capability thresholds
  -> quality/resource envelope per quantization
  -> minimum viable capability / actor map
  -> resource-aware execution plan
  -> observed migration results
  -> revised thresholds
```

The thresholds are provisional planning evidence, not permanent properties of a model. They may change with better prompts, trusted context, compiler-derived facts, VSlices discovery constraints, Ruleset evolution, context-cache settings, hardware, thermal/power conditions, or the migration corpus itself.

## 13. Progress criteria

Do not measure progress primarily by number of files translated.

Prefer evidence such as:

```text
named concepts cover more of the objective
associations become more stable
reorganization reduces accidental source-layout coupling
semantic declarations are increasingly justified
unknowns remain explicit
discovery exposes useful next decisions without guessing
structured values can be composed from advertised grammar
more concepts reach authoring parity
lowered witnesses satisfy relevant compile/test/runtime evidence
feedback returns cleanly into semantic reconstruction
resource-aware execution assigns only as much model capability as an operation has demonstrated it needs
resource planning accounts for RAM, KV cache, paging, throughput and parallelism rather than model quality alone
escalations distinguish missing capability from missing context, missing authority and Tooling gaps
```

## 14. Anti-patterns

Avoid:

```text
translating classes one-to-one before identifying concepts
inventing kind/classification because a section is available
using tags as semantic truth
organizing only by original folders/namespaces
waiting for total understanding before creating artifacts
requiring every artifact to be complete before it can exist
bypassing discovery with secret client-side grammar knowledge
using add because a YAML key is absent when set establishes the assertion
lowering incomplete semantics and compensating with target guesses
allowing target renderer lookup to create semantic authority
patching materialized code instead of returning evidence to the semantic model
letting conventions override explicit semantic relations
assuming later reorganization invalidates earlier evidence rather than refining it
assigning the strongest available model to every operation without evidence that the additional capability is required
ranking quantizations only by answer quality or tokens/second while ignoring memory pressure, paging, context capacity and parallel composition
escalating model size when the actual blocker is missing context, authority, Tooling support or conflicting evidence
```

## 15. Evolution of this plan

This is a baseline, not a final methodology.

When exercising it against real migrations, record where:

```text
an AI had to assume too much
discovery exposed too much or too little
grammar-driven affordances were insufficient
concept naming happened too early or too late
tags failed to support useful reorganization
coherent-scope boundaries were difficult to determine
semantic detailing lacked an intermediate step
lowering happened too early or too late
authoring/lowering parity broke
feedback from executable evidence was not fed back cleanly
minimum viable capability estimates failed to transfer to real work
resource measurements failed to predict practical throughput or coexistence
context/KV-cache cost changed which quantization was practically viable
paging or thermal/power conditions distorted benchmark comparisons
small-worker parallelism increased coordination cost more than throughput
escalations were routed to the wrong actor class
context/tooling improvements changed the capability threshold for an operation
```

Those observations should revise this plan rather than accumulate migration-specific workarounds.