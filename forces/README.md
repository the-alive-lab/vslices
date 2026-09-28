# Work forces

## Status

`candidate`

## Ownership affinity

`Design` currently has the strongest ownership affinity.

The model is preserved here because it affects cross-product movement between organizational understanding and system realization.

## Purpose

Work forces bias the direction, origin, destination, and cost of engineering effort.

They are not exclusive territories.

Every meaningful effort may be affected by every force group, but some forces tend to emphasize particular regions or movements.

## Semantic forces

### Priority

Deep understanding of the business and the work.

### Typical emphasis

- upper half of the Organization / System work space;
- organizational side of the space;
- abstraction and contextual understanding;
- preservation of meaning, authority, and continuity.

Typical questions:

- What work actually exists?
- Why does it exist?
- Who owns the decision?
- What meaning would be lost if we only inspected the software?

## Technical forces

### Priority

Reduction of technical complexity while preserving honest semantics.

### Typical emphasis

- central Organization / System overlap;
- Process / Flow relationships;
- candidate responsibility boundaries;
- system composition and segmentation.

Useful criteria may include:

- coherence;
- cohesion;
- coupling;
- explicit authority;
- consistency;
- manageable dependencies.

These criteria are contextual tools, not a mechanical score.

## Delivery forces

### Priority

Fast useful feedback and resolution of urgent needs.

### Typical emphasis

- lower parts of the work space;
- system-facing realization;
- movements that reach executable feedback sooner;
- reduction of unnecessary movements.

Delivery pressure may justify a smaller or more incremental realization.

It does not authorize semantic contradiction, hidden loss of invariants, or invented authority.

## Resource forces

### Priority

Use of scarce resources, including money, people, infrastructure, time, and cognitive capacity.

### Typical emphasis

- reduce the number of movements;
- reduce transformation cost;
- reuse existing knowledge and realization where appropriate;
- avoid work whose expected value does not justify its cost.

## Directionality

Forces help determine:

```text
where effort starts
-> which transformations are worth performing
-> where effort should converge
```

They therefore influence, but do not fully determine, modality and planning.

## Relationship with Action Flow movements

Current Action Flow movements include candidates such as:

- Concretize;
- Abstract;
- Digitize;
- Materialize;
- Compose;
- Segment.

Forces may favor different combinations.

Example:

```text
Organization / Process
    -- Digitize --\
                   -> System / Process
System / Flows
    -- Compose ---/
```

Strong delivery pressure may favor reusing current System / Flows.

Strong semantic pressure may first require more work on the Organization / Process side.

Strong resource pressure may reduce the number of transformations attempted in the current iteration.

## Relationship with modalities

A candidate interpretation is that Design modalities are strategies for navigating the work space under different uncertainty and force profiles.

For example:

- Context-First may be favored when semantic uncertainty is broad;
- Problem-First may be favored when a localized pressure is visible within an understood context;
- Slice-First may be favored when enough is known to seek implementation feedback safely.

This relationship remains candidate and should be validated through repeated real use.
