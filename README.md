# Invariant Thinking

**A framework for learning and reasoning under accelerated technological change.**

Invariant Thinking is an open conceptual framework for separating **transferable structure** from **implementation-specific novelty**. Its purpose is practical: when a new technology appears, do not relearn the entire surface. Identify what remains structurally true, test the limits of that mapping, and invest deep learning effort in the **actual delta**.

> Learn what survives the change.

## Status

**Draft 0.1 — open proposal.**

Invariant Thinking is not presented as a scientifically validated theory of cognition. It is a structured framework, vocabulary, and repeatable method intended for use, criticism, case studies, and future empirical evaluation.

## The problem

In fast-moving technical domains, tools, frameworks, APIs, interfaces, and product categories change faster than a practitioner can study each manifestation independently. A purely implementation-centered learning strategy creates recurring cognitive rework.

Invariant Thinking proposes a different unit of learning:

```text
product -> implementation -> mechanism -> pattern -> constraint -> invariant
```

The deeper the reusable structure, the more future systems it may help explain. The framework does **not** assume that everything new is merely old technology with new branding. Its method explicitly searches for where analogies fail and where genuine novelty begins.

## Core model

### The Invariant Stack

| Layer | Question | Typical volatility |
|---|---|---:|
| L5 — Product / Interface | What do users or developers interact with? | High |
| L4 — Implementation | How is the capability concretely built? | High |
| L3 — Mechanism | By what mechanism does it work? | Medium-high |
| L2 — Pattern | What recurring organization solves this class of problem? | Medium |
| L1 — Constraint | What limits the solution space? | Low-medium |
| L0 — Invariant | What relevant property must remain true across the defined transformation? | Context-dependent, often low |

An invariant is never claimed in isolation. A valid Invariant Thinking statement identifies:

1. the **property** claimed to remain relevant;
2. the **transformation set** across which it is being compared; and
3. the **boundary** within which the claim is intended to hold.

## The DELTA Protocol

The operational method is **DELTA**:

1. **Decompose** — break the system into actors, state, inputs, outputs, boundaries, resources, transformations, and dependencies.
2. **Extract** — identify constraints and candidate invariants.
3. **Link** — map those structures to prior knowledge and known patterns.
4. **Test** — actively search for where the analogy, invariant, or prior model breaks.
5. **Acquire** — learn the irreducible delta that remains.

The conceptual relation is:

```text
new system
- correctly transferable prior knowledge
= learning delta
```

This is a reasoning aid, not a quantitative equation.

## Four canonical questions

Every Invariant Thinking analysis should be able to answer:

1. **What changed?**
2. **What remained true?**
3. **Under which transformation and boundary?**
4. **Where does the analogy break?**

If the fourth question is missing, the analysis is incomplete.

## What this repository contains

- [`SPEC.md`](SPEC.md) — normative definition of the framework.
- [`DELTA-PROTOCOL.md`](DELTA-PROTOCOL.md) — operational procedure.
- [`PRINCIPLES.md`](PRINCIPLES.md) — design principles.
- [`GLOSSARY.md`](GLOSSARY.md) — controlled terminology.
- [`NON-CLAIMS.md`](NON-CLAIMS.md) — explicit statements the framework does not make.
- [`LIMITATIONS.md`](LIMITATIONS.md) — known weaknesses and failure modes.
- [`PRIOR-ART.md`](PRIOR-ART.md) — intellectual context and related work.
- [`RESEARCH.md`](RESEARCH.md) — testable hypotheses and research agenda.
- [`examples/`](examples/) — worked analyses.
- [`maps/template.yaml`](maps/template.yaml) — reusable Invariant Map format.
- [`rfcs/`](rfcs/) — proposed changes to the framework.

## Quick example

A new framework introduces server-side function invocation directly from UI code.

A shallow reading says: "this replaces APIs."

An Invariant Thinking analysis asks:

- **Changed:** invocation ergonomics, routing abstraction, framework integration.
- **Candidate invariants:** trust boundaries, authorization, validation, serialization, failure, latency.
- **Boundary:** multi-user network applications invoking privileged server behavior.
- **Analogy break:** framework-mediated actions are not semantically identical to public REST endpoints.
- **Learning delta:** framework-specific execution, serialization, caching/revalidation, lifecycle, and security semantics.

The goal is not to deny novelty. The goal is to locate it accurately.

## Contribution standard

A contribution must do more than assert that two technologies are "basically the same." It should identify the transformation, state the invariant boundary, provide evidence or reasoning, and include at least one plausible analogy break or counterexample.

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Prior art and intellectual honesty

Invariant Thinking builds on long-standing ideas around invariance, abstraction, structural reasoning, analogy, schema formation, and transfer. The claim of this project is **not** that the word *invariant* or the general value of abstraction is new.

The proposed contribution is the specific combination of:

- the **Invariant Stack**;
- **Transformation + Boundary** as required context for invariant claims;
- the **Learning Delta** as the target of deep learning effort;
- the **DELTA Protocol**;
- **Invariant Maps** as a reusable analysis artifact; and
- explicit **analogy-break testing** as a guard against reductionism.

See [`PRIOR-ART.md`](PRIOR-ART.md).

## Citation

If you use or discuss this framework, see [`CITATION.cff`](CITATION.cff).

## License

The conceptual and written material in this repository is licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**. See [`LICENSE.md`](LICENSE.md).
