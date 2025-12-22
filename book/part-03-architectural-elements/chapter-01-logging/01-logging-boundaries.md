# Logging Boundaries

## Responsibility

The responsibility of logging in this architecture is **observation without influence**.

Logging exists to record meaningful events, failures, and execution context so that system behavior can be understood after the fact. It must never participate in decision-making or alter execution flow.

Logging observes the system; it does not steer it.

---

## Why Logging Requires Boundaries

Without explicit boundaries, logging becomes a hidden source of coupling.

When logs are used to drive decisions, enforce rules, or replace validation, they cease to be observational and begin to shape behavior. Over time, this erodes architectural clarity and introduces invisible dependencies.

Logging boundaries exist to ensure that:

- Behavior is defined by code, not instrumentation
- Failures are handled explicitly, not inferred
- Observability does not become control flow

---

## What Logging Is Allowed to Do

Logging may:

- Record entry and exit points
- Capture failure context
- Report unexpected states
- Provide correlation and trace information
- Assist with diagnostics and post-mortem analysis

Logging may describe *what occurred* and *where*.

---

## What Logging Must Never Do

Logging must not:

- Influence branching or control flow
- Replace validation or error handling
- Be required for correctness
- Encode business rules
- Determine outcomes based on log state

If the system behaves differently depending on whether logging is enabled, the boundary has been violated.

---

## Layer-Specific Boundary Rules

### Presentation Layer

Presentation logging may:

- Log request receipt and completion
- Capture malformed input
- Record authentication or transport failures

Presentation logging must not interpret application behavior or infer domain outcomes.

---

### Application Layer

Application logging may:

- Record use-case execution boundaries
- Log orchestration progress and failure context
- Capture handler-level execution details

Application logging must not encode business rules or workflow decisions.

---

### Domain Layer

The Domain layer does not log.

Domain behavior must be observable through outcomes, not instrumentation. Logging inside the Domain would introduce coupling to infrastructure concerns and violate domain purity.

---

### Infrastructure Layer

Infrastructure logging may:

- Capture persistence failures
- Record integration or transport errors
- Log retry, timeout, or resource conditions

Infrastructure logs must not leak implementation details upward or dictate application behavior.

---

## Relationship to Error Handling

Logging and error handling serve different purposes:

- **Errors** control execution
- **Logs** describe execution

An error may be logged, but a log must never substitute for error signaling.

When error handling relies on logs to function, the architecture has failed to enforce boundaries.

---

## Consequences of Boundary Violation

When logging boundaries are violated:

- Control flow becomes implicit
- Debugging replaces reasoning
- Behavior depends on environment configuration
- The system becomes fragile under change

Over time, logging ceases to provide clarity and instead becomes a liability.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-logging-placement.md">Next ▶</a>
</p>
