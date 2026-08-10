# Invariant Map — Tool-Using AI Agents

## Subject

Transition from deterministic workflow automation to LLM-mediated systems that select and invoke tools.

## Purpose

Identify which workflow and distributed-systems concepts transfer, and where probabilistic model behavior creates a real delta.

## Transformation

```text
explicit deterministic orchestration -> model-mediated action selection
```

## Boundary

Software agents that receive goals or instructions, maintain some context, and can invoke external tools or services.

## Decompose

- Input or goal.
- Context/state.
- Decision mechanism.
- Tool registry/capabilities.
- Tool invocation.
- External side effects.
- Observation/result.
- Repetition or termination.

## Candidate invariants

- Side effects still require authority and control.
- External calls still fail and need observable outcomes.
- State still needs ownership, persistence, and consistency semantics.
- Tool interfaces still require contracts.
- Untrusted inputs and outputs still cross trust boundaries.
- Idempotency remains relevant for retryable side effects.

## Changed properties

- Action selection can be probabilistic.
- Natural language may participate in control flow.
- The decision policy may not be directly inspectable as conventional code.
- Prompt/context composition can alter behavior.
- Model capability changes can modify effective system behavior without ordinary source-code changes.

## Prior-model links

- Workflow engines.
- Planners.
- State machines.
- Tool/plugin architectures.
- Distributed job execution.

## Analogy breaks

A tool-using LLM agent cannot be modeled completely as a deterministic state machine without losing behaviorally relevant uncertainty. Model inference introduces failure modes and control characteristics that ordinary explicit orchestration may not share.

## Learning Delta

- model uncertainty and evaluation;
- tool-selection reliability;
- prompt/context security;
- model-specific failure modes;
- guardrail architecture;
- observability for probabilistic decisions;
- cost/latency characteristics of inference.

## Unknowns

The boundary between model behavior and orchestrator behavior varies substantially by architecture and must be stated per system.
