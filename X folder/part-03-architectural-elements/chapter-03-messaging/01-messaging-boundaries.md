# Messaging Boundaries

## Responsibility

The responsibility of messaging in this architecture is **decoupling execution timing without obscuring intent**.

Messaging allows work to occur asynchronously, but it must never hide *what* is happening, *why* it is happening, or *who* is responsible for initiating it.

Messaging changes *when* work happens—not *what* the system does.

---

## Why Messaging Requires Boundaries

Asynchronous communication introduces indirection.

Without clear boundaries, messaging can quickly become a mechanism for hiding behavior, bypassing architectural entry points, or distributing business logic across loosely connected consumers.

Messaging boundaries exist to ensure that:

- Application behavior remains explicit
- Execution paths remain understandable
- Responsibility is clearly owned
- Asynchronous work does not replace orchestration

---

## What Messaging Is Allowed to Do

Messaging may:

- Decouple producers and consumers
- Allow work to proceed asynchronously
- Improve resilience under load or partial failure
- Enable eventual consistency where appropriate

Messaging may change *execution timing*, but it must preserve *execution intent*.

---

## What Messaging Must Never Do

Messaging must not:

- Replace application orchestration
- Encode business rules
- Introduce implicit behavior
- Bypass application entry points
- Become required for correctness

If understanding system behavior requires tracing message consumers instead of application intent, the boundary has been violated.

---

## Messaging and Determinism

Asynchronous execution does not excuse ambiguity.

Even when work is deferred:

- The initiating intent must be explicit
- The expected outcome must be defined
- Failure paths must be understood

Messaging introduces concurrency; it must not introduce uncertainty.

---

## Relationship to Architectural Boundaries

Messaging must respect existing architectural boundaries.

- All messaging originates from explicit application intent
- Infrastructure delivers messages but does not decide *when* to send them
- Consumers handle messages within well-defined responsibilities

Messaging flows *through* the architecture—it does not redefine it.

---

## Consequences of Boundary Violation

When messaging boundaries are violated:

- Behavior becomes emergent rather than intentional
- Debugging requires tracing distributed side effects
- Responsibility becomes unclear
- Change becomes risky and expensive

Messaging shifts from an architectural tool to an architectural liability.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-commands-vs-events.md">Next ▶</a>
</p>
