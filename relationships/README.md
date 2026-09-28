# Relationships

## Purpose

VSlices needs to distinguish definition authority from the ways a definition is used or realized.

Candidate relationships include:

- `owned-by`;
- `used-by`;
- `implemented-by`;
- `realized-by`;
- `preserved-by`;
- `rendered-by`;
- `operationalized-by`;
- `supported-by`;
- `challenged-by`;
- `derived-from`;
- `supersedes`.

This is not yet a stable schema.

## Core distinction

```text
physical location
!= semantic authority

implementation
!= definition

automation
!= authority
```

## Action Flow

```text
Action Flow
    owned-by -> VSlices Suite
    used-by -> Design
    used-by -> Method
    realized-by -> Docs Standard diagram notation
    operationalized-by -> Tooling (future candidate)
    related-to -> Framework realization when justified
```

## Semantic Pressure

```text
Semantic Pressure
    owned-by -> VSlices Suite
    used-by -> Design
    used-by -> Method
    preserved-by -> Docs Standard
    operationalized-by -> Tooling (possible future)
```

## Organization / software continuity

A current candidate relationship is:

```text
Business Scenario
    -> organizational view of work

Software Project
    -> systematized view of work
```

Normal VSlices use should attempt to preserve continuity between those perspectives proactively.

`Traceability` becomes especially relevant when continuity must be reconstructed, verified, or repaired reactively.

This interpretation remains candidate and must be tested against existing Continuity Path semantics before promotion.
