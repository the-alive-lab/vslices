# Action Flow

## Status

`candidate`

## Ownership

`VSlices Suite`

## Purpose

An **Action Flow** represents work through ordered actions, conditions, consequences, participants, and relevant relationships between actions.

Its purpose is to let work be elaborated progressively from an organizational perspective toward a systematized perspective without conflating both.

## Main projections

### Abstract Action Flow

Represents work without committing to a concrete realization.

It may show:

- actions;
- ordering;
- conditions;
- cardinality;
- consequences;
- actors or roles when semantically relevant;
- handoffs;
- alternatives;
- repetition.

Its natural affinity is organizational understanding.

### Systematized Action Flow

Represents how work is, or is proposed to be, realized by human actors and system responsibilities.

Possible responsibility lanes include:

```text
Human
  External User
  Internal User
  Reviewer

System
  View
  Product / BFF
  Service
  Worker
  Provider
```

Lane identity should express useful responsibility for the current decision.

It does not automatically imply a repository, process, deployment, project, or service boundary.

## Work elaboration space

Action Flow currently relates to this work hierarchy:

```text
Scenario
  -> Work Line
      -> Work Process
          -> Work Flow
              -> Work Step
```

Two directions are naturally useful.

### Organizational concretization

```text
Work Line
-> Work Process
-> Work Flow
```

The useful organizational descent often stops at Flow because going below it generally requires concrete, instructive realization detail.

### System composition

```text
Work Step
-> Work Flow
-> Work Process
```

The useful realization ascent often stops at Process because moving from Process to Work Line requires organizational knowledge that should not be inferred safely from system realization alone.

## Organization / System matrix

```text
                    ORGANIZATION        SYSTEM
                  +----------------+----------------+
Line              | Work Line      |       -        |
Process           | Work Process   | Work Process   |
Flow              | Work Flow      | Work Flow      |
Step              |       -        | Work Step      |
                  +----------------+----------------+
```

Process and Flow form the overlap where organizational work and system realization can remain connected without being treated as equivalent.

## Candidate movements

### Concretize

```text
Organization / Line
-> Organization / Process
```

Question:

> We recognize these work lines. What processes realize them, how do they begin, and what relationships or dependencies do they have?

### Abstract

```text
Organization / Process
-> Organization / Line
```

Question:

> We have these processes, inputs, and outputs. What larger coordinated work do they reveal?

### Digitize

```text
Organization / Process
-> System / Process
```

Seeks a systematized realization of an organizational process.

### Materialize

```text
System / Flow
-> Organization / Flow
```

Seeks to recognize what organizational work an observed system realization materializes.

The name remains candidate because `materialization` is used in the opposite direction in other VSlices contexts.

### Compose

```text
System / Flow
-> System / Process
```

Composes several systematized actions or capabilities into a larger process responsibility.

### Segment

```text
System / Process
-> System / Flow
```

Splits an overly broad realization so that differentiated responsibilities or actions become visible.

## Compound effort

Several transformations may converge toward one design objective.

Example:

```text
Organization / Processes
    -- Digitize --\
                   -> System / Process
System / Flows
    -- Compose ---/
```

This supports questions such as:

> The organization needs this process and the system already has these capabilities. How do we compose a realization that moves both toward the same objective?

Transformations with a common destination may belong to one related effort.

Different destinations should normally remain independent efforts even if they share evidence or source material.

## Product relationships

### Design

May use Action Flow to reason about work, responsibilities, candidate boundaries, and realization.

### Method

May decide when to create, deepen, compare, or revisit Action Flows during the lifecycle.

### Docs Standard

May define documentary and visual realizations of the mechanism, including metadata, notation, preservation, and artifact relationships.

### Tooling

May eventually support authoring, validation, transformation, navigation, or rendering.

### Framework

May relate systematized Action Flows to executable semantics where continuity is justified, without assuming automatic equivalence between documentary Work Flow and runtime Flow.

## Limits

Action Flow does not decide architecture by itself.

It does not imply:

- one Feature per action;
- one Service per lane;
- one deployment per responsibility;
- identical organizational and system structures.

Its value is making transformations between perspectives visible.
