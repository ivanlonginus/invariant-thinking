# Invariant Thinking Framework Specification

**Version:** 0.1-draft
**Status:** Open proposal
**Canonical language:** English

## 1. Purpose

Invariant Thinking Framework (ITF) defines a disciplined way to reason about unfamiliar or changing systems by distinguishing transferable structural knowledge from implementation-specific novelty.

The framework is intended for domains where manifestations change quickly enough that repeatedly learning each implementation from scratch is inefficient.

## 2. Scope

ITF specifies:

- a vocabulary for structural comparison;
- a layered analysis model (the Invariant Stack);
- requirements for making invariant claims;
- the DELTA Protocol for analyzing unfamiliar systems;
- an Invariant Map artifact for documenting an analysis; and
- validation and falsification expectations.

ITF does not prescribe a curriculum, guarantee faster learning, or claim universal cognitive laws.

## 3. Normative language

The keywords **MUST**, **MUST NOT**, **SHOULD**, **SHOULD NOT**, and **MAY** indicate requirements within this specification. They describe conformance to this framework, not scientific necessity.

## 4. Core definitions

### 4.1 System

A bounded subject of analysis whose behavior, structure, implementation, or use is being compared with another state, system, or model.

### 4.2 Transformation

A defined change from one system state, representation, implementation, interface, architecture, or context to another.

A transformation MAY change some properties while preserving others.

### 4.3 Invariant

A property considered to remain relevantly unchanged across a **specified transformation set**, within a **specified boundary**.

An ITF invariant claim MUST NOT be expressed as an unqualified statement that something "never changes."

### 4.4 Invariant Boundary

The context in which an invariant claim is intended to hold. It may include domain, actor, scale, threat model, execution model, physical constraints, or other assumptions.

### 4.5 Learning Delta

The knowledge that remains genuinely necessary after correctly transferable prior knowledge has been identified and validated.

The Learning Delta is conceptual; ITF 0.1 does not define a numeric measure for it.

### 4.6 Analogy Break

A condition under which a proposed structural mapping ceases to preserve the property relevant to the analysis.

A conforming analysis MUST attempt to identify at least one analogy break, failed mapping, or boundary condition.

## 5. Invariant Stack

ITF uses six analytical layers. They are not asserted to be ontologically universal; they are a practical decomposition.

### L5 — Product / Interface

The named product, surface, syntax, API, interaction model, or externally visible capability.

### L4 — Implementation

The concrete realization of a capability, including libraries, runtime choices, algorithms, deployment details, and internal composition.

### L3 — Mechanism

The process by which an outcome is produced: message passing, indexing, caching, replication, rendering, scheduling, etc.

### L2 — Pattern

A recurring organization of mechanisms that addresses a class of problems: client/server, observer, pipeline, pub/sub, event loop, actor model, etc.

### L1 — Constraint

A condition restricting possible solutions: latency, finite memory, trust, consistency, failure, bandwidth, concurrency, cost, regulation, physical limits, etc.

### L0 — Invariant

A relevant property that remains preserved across the transformation being analyzed, within its declared boundary.

## 6. Valid invariant claim

A valid ITF invariant claim MUST identify all of the following:

- **Property** — what is claimed to remain true.
- **Transformation** — what is changing.
- **Boundary** — where the claim applies.
- **Reasoning or evidence** — why the property is expected to persist.
- **Break condition** — a case where the claim may cease to hold.

Example:

> In multi-user applications that execute privileged server behavior, the need to enforce authorization remains across transformations from REST endpoints to framework-mediated server actions, unless the execution boundary itself is removed or all actions become non-privileged and non-user-specific.

## 7. DELTA Protocol

A conforming ITF analysis SHOULD follow the DELTA Protocol in order:

1. **Decompose** the target system.
2. **Extract** constraints and candidate invariants.
3. **Link** them to prior models.
4. **Test** the mappings and boundaries.
5. **Acquire** the remaining Learning Delta.

See [`DELTA-PROTOCOL.md`](DELTA-PROTOCOL.md).

## 8. Invariant Map

A reusable ITF analysis SHOULD be recorded as an Invariant Map containing:

- subject;
- purpose;
- source and target contexts;
- transformation;
- boundary;
- decomposition;
- candidate invariants;
- prior-model links;
- changed properties;
- analogy breaks;
- learning delta;
- unknowns;
- confidence and evidence notes.

See [`maps/template.yaml`](maps/template.yaml).

## 9. Validation rules

An analysis is stronger when it:

- distinguishes similarity from invariance;
- defines the transformation rather than comparing vague categories;
- names assumptions and boundaries;
- records counterexamples;
- distinguishes known facts from inference;
- updates the map when contradictory evidence appears.

## 10. Anti-reductionism requirement

ITF MUST NOT be used to conclude that a new system is "nothing new" merely because some lower-level properties map to older concepts.

The existence of shared invariants does not imply identical mechanisms, implementations, capabilities, economics, scale, or consequences.

## 11. Lossy Abstraction Principle

Every abstraction suppresses variation. An abstraction is useful only when the discarded variation is irrelevant to the reasoning task at hand.

Accordingly, ITF analyses MUST treat excessive abstraction as a failure mode rather than a mark of sophistication.

## 12. Versioning

Changes to normative definitions SHOULD be proposed through RFCs and recorded in `CHANGELOG.md`.

The framework uses semantic-style public versions for communication, but pre-1.0 versions remain experimental.
