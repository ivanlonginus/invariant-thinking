# Invariant Map — Framework-Mediated Server Actions

> This is a conceptual example, not a substitute for the security documentation of any specific framework.

## Subject

Moving from explicit HTTP API handlers to framework-mediated server function invocation from application UI code.

## Purpose

Determine which prior web-application concepts transfer and what must still be learned.

## Transformation

```text
explicit endpoint invocation -> framework-mediated server invocation
```

## Boundary

Multi-user network applications in which client-originated intent can cause privileged server-side behavior.

## Decompose

- Client expresses an action.
- Information crosses a client/server boundary.
- Server code receives data.
- Server may read or mutate protected resources.
- Execution can fail.
- Results or invalidation state return to the application.

## Candidate invariants

- Untrusted input still requires validation where correctness or safety depends on it.
- Privileged behavior still requires authorization.
- Network or distributed execution still admits failure and latency.
- Data crossing boundaries still requires a representation/serialization contract.
- Mutations still require consistency decisions.

## Changed properties

- Invocation ergonomics.
- Routing visibility.
- Framework ownership of request construction.
- Integration with rendering, caching, and invalidation.
- Deployment/runtime semantics.

## Prior-model links

- RPC.
- Request/response communication.
- Command handlers.
- Server-side mutation endpoints.

## Analogy breaks

A server action is not automatically equivalent to a public REST endpoint. Framework lifecycle, serialization constraints, caching behavior, invocation surface, and transport abstraction can materially differ.

## Learning Delta

Study the specific framework's:

- execution boundary;
- serialization rules;
- authentication/authorization integration;
- caching/revalidation semantics;
- failure behavior;
- deployment/runtime constraints.

## Unknowns

Runtime- and framework-version-specific behavior must be verified against current primary documentation.
