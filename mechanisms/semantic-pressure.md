# Semantic Pressure

## Status

`candidate`

## Ownership

`Method`

## Applicability

`VSlices Suite`

## Purpose

**Semantic Pressure** is a methodological VSlices mechanism for deliberately continuing semantic interrogation while each answer still exposes a distinction that is material to the resolution.

Its purpose is not to ask "why" repeatedly.

Historically, the practice was described informally as **"porquear para porquenuar"**. In that expression, *porquear* does not mean literally asking `why?`. It means pressing on what is not yet understood well enough by asking the question that best exposes the next relevant distinction.

Depending on the situation, that question may be causal, explanatory, definitional, operational, epistemic, authoritative, consequential, or otherwise semantic.

Examples include:

- Why is that?
- How is that?
- What do you mean by that?
- In what sense?
- How does that work?
- Who decides that?
- How do we know that?
- What does that imply?
- What happens if this changes?

The important property is not the wording of the question.

The mechanism continues while an answer reveals something that remains materially relevant to understanding or conducting the resolution, such as:

- meaning;
- distinctions;
- assumptions;
- constraints;
- authority;
- provenance;
- consequences;
- invariants;
- decisions;
- available evidence;
- missing evidence;
- what is determined;
- what remains open.

A compact working description is:

> Semantic Pressure is the deliberate continuation of semantic interrogation while each answer exposes a distinction, assumption, authority, constraint, consequence, or evidence gap that remains material to the resolution.

## Methodological ownership

Its conceptual ownership belongs to **Method** because Method has a second-order responsibility: it provides criteria, techniques, and mechanisms for using, connecting, interrogating, or conducting one or more VSlices surfaces during a resolution.

Its applicability is suite-wide.

This distinction is intentional:

```text
ownership != applicability

Method
  owns Semantic Pressure
        |
        +-- applicable across the suite
              +-- Design
              +-- Docs Standard
              +-- Framework
              +-- other participating surfaces
```

Cross-product use does not make Design, Docs Standard, Framework, or other products co-owners of the mechanism.

## Semantic Pressure is not an interrogation technique

Semantic Pressure does not need to own the concrete questioning or elicitation technique used to perform the interrogation.

Depending on the pressure being examined, Method may use or combine techniques preserved by Design or supplied by external disciplines.

Possible examples include:

- assumption surfacing;
- requirements elicitation;
- critical questions;
- Socratic or guided questioning;
- domain-specific inquiry techniques;
- other methods appropriate to the situation.

Therefore:

```text
Semantic Pressure
    -> decides where, why, how far, and until when
       semantic scrutiny is needed

interrogation technique
    -> provides one possible way to perform that scrutiny
```

This distinction prevents Semantic Pressure from claiming ownership over questioning techniques merely because it can use them.

## Continuation rule

A useful informal model is:

```text
statement / concept / model / decision / representation
    ↓
appropriate semantic interrogation
    ↓
answer
    ↓
does the answer expose another material distinction?
    ├── yes -> continue pressure
    ├── no  -> continue the resolution
    └── requires external knowledge
              -> stop inference
              -> obtain evidence
```

This is the practical meaning historically captured by "porquear para porquenuar": continue interrogating when the answer itself creates a legitimate next surface of understanding.

## Stopping rule

Semantic Pressure does not exist to maximize questions or depth.

It should stop when:

- relevant uncertainty has been reduced sufficiently to continue responsibly;
- the next interrogation is unlikely to change the resolution materially;
- further depth would be ornamental rather than useful;
- or missing knowledge must be obtained through external evidence rather than inferred.

Stopping is part of the mechanism.

Without a stopping rule, semantic interrogation can degrade into unlimited depth without proportional value.

## Typical pressure targets

Semantic Pressure may be applied to a:

- term;
- claim;
- explanation;
- assumption;
- model;
- boundary;
- responsibility;
- decision;
- document;
- method;
- representation;
- implementation;
- observed behavior;
- relationship between artifacts.

Typical pressure may expose questions such as:

- What exactly does this term mean?
- How is that?
- What distinguishes it from a similar concept?
- Who has authority to establish this fact?
- What must be true before or after?
- What evidence is needed?
- Where can that evidence come from?
- What can be derived and what must be observed?
- What can fail in an expected way?
- What changes as a consequence?

These are examples of possible pressure, not a proprietary or exhaustive question catalog.

## Product relationships

### Method

Owns the base methodological meaning of Semantic Pressure.

Method may decide:

- where semantic pressure is needed;
- why it matters to the current resolution;
- what dimension requires further interrogation;
- which interrogation technique is appropriate;
- how far to continue;
- when additional evidence is required;
- and when to stop.

Method may apply Semantic Pressure during resolutions that involve several products simultaneously.

### Design

May be interrogated through Semantic Pressure to deepen understanding and challenge candidate models, boundaries, distinctions, methodologies, or other forms of resolution.

Design may also preserve reusable interrogation techniques that Method can select or combine when applying Semantic Pressure.

Use by Design does not transfer ownership of the mechanism.

### Docs Standard

May preserve distinctions, uncertainties, decisions, provenance, authority, or evidence exposed through Semantic Pressure.

It consumes the results without owning the methodological mechanism.

### Framework

May represent meaning, authority, restrictions, evidence, degrees of determination, or behavior made explicit through Semantic Pressure when those distinctions need to survive into later representations or realizations.

It consumes the results without owning the methodological mechanism.

### Tooling

May assist application, prompting, navigation, validation, evidence lookup, or preservation related to Semantic Pressure without gaining authority over its methodological meaning or over the answers it helps expose.

## Reconstructed evolution

Semantic Pressure originated as a candidate Method technique.

Its earlier informal use included the practice described as **"porquear para porquenuar"**: continue interrogating what is not sufficiently understood, using whichever question exposes the next relevant distinction.

Later use showed that it could be applied across several VSlices products and resolutions involving multiple surfaces.

That cross-product applicability was temporarily interpreted as suite-level ownership.

The ownership distinction was later corrected.

The current clarification also makes explicit that Semantic Pressure is not itself a proprietary questioning technique or question catalog.

The reconstructed trajectory is therefore:

```text
informal practice: "porquear para porquenuar"
-> candidate Method technique
-> observed cross-product applicability
-> mistaken provisional inference: suite-level ownership
-> ownership/applicability distinction clarified
-> Method-owned mechanism with suite-wide applicability
-> interrogation mechanism distinguished from concrete interrogation techniques
```

The preserved lessons are:

```text
scope of applicability
!=
conceptual ownership

semantic interrogation
!=
asking "why" literally

Semantic Pressure
!=
the concrete interrogation technique it may use
```

This trajectory is preserved so the current definition does not rewrite history as if every distinction had always been explicit.
