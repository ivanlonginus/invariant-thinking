# DELTA Protocol

DELTA is the operational method of Invariant Thinking.

Its objective is to reduce unnecessary relearning without hiding genuine novelty.

## D — Decompose

Describe the target without relying on its marketing category.

Capture at minimum:

- actors;
- inputs and outputs;
- state;
- transformations;
- boundaries;
- resources;
- dependencies;
- failure modes;
- trust assumptions.

Questions:

- What does the system actually do?
- Where is state held?
- Which components communicate?
- Which actions cross a trust or process boundary?
- What can fail independently?

**Output:** a neutral structural description.

## E — Extract

Identify constraints and candidate invariants.

Questions:

- What conditions still have to be satisfied regardless of implementation?
- Which constraints are imposed by physics, information, economics, trust, or the problem definition?
- If the product disappeared tomorrow, which problem would still exist?

Every candidate invariant must be written with a transformation and boundary.

**Output:** candidate invariant statements.

## L — Link

Map the decomposition to prior knowledge.

Questions:

- Which mechanisms or patterns are already known?
- Which previous systems share the relevant relations?
- Is the similarity structural or merely visual/terminological?

Do not force a mapping. An unmapped component is useful information.

**Output:** prior-model links and unmapped areas.

## T — Test

Try to falsify the transfer.

Questions:

- Where does the analogy stop working?
- Which candidate invariant actually changed?
- Which new constraint invalidates the old model?
- Does scale change the mechanism qualitatively?
- Is the old model missing a capability that changes what is possible?

This stage exists to prevent "everything is the same underneath" reasoning.

**Output:** analogy breaks, boundary corrections, rejected invariants.

## A — Acquire

Study the remaining Learning Delta.

Prioritize:

1. genuinely new mechanisms;
2. changed constraints;
3. changed boundaries;
4. implementation semantics that affect correctness;
5. operational details required for current work.

Deprioritize memorization that can be cheaply retrieved and does not improve the structural model.

**Output:** an explicit learning agenda.

## Completion criteria

A DELTA analysis is complete enough for practical use when it can answer:

- What changed?
- What remained true?
- Under what transformation and boundary?
- Where does the analogy break?
- What do I still need to learn?

## Failure signal

If the analysis produces almost no Learning Delta for a genuinely unfamiliar system, assume the abstraction may be too coarse and repeat **Test**.
