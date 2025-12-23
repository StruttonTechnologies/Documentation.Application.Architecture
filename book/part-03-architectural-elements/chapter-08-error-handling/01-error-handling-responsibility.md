# Error Handling Responsibility

## Responsibility

The responsibility of error handling in this architecture is to **detect, represent, and propagate failure without altering intent, behavior, or business outcomes**.

Error handling makes failure explicit and observable. It does not decide what should happen next, nor does it attempt to recover implicitly.

---

## Why This Responsibility Exists

Failure is inevitable.

Systems fail due to invalid input, rule violations, infrastructure faults, concurrency conflicts, or unexpected conditions. Without clear error handling boundaries, failures become hidden, misinterpreted, or silently absorbed, leading to ambiguous behavior and loss of trust.

Error handling exists to ensure that:

- Failures are visible and explicit
- Execution intent is preserved under failure
- Responsibility for failure is traceable
- Behavior remains intentional and deterministic

Error handling clarifies failure; it does not resolve it.

---

## What Error Handling Is Allowed to Do

Error handling may:

- Detect and surface failures
- Preserve contextual information about errors
- Propagate failure consistently across boundaries
- Distinguish failure from success
- Prevent silent continuation after failure

Error handling may stop execution, but it must never redefine execution.

---

## What Error Handling Must Never Do

Error handling must not:

- Encode business rules
- Perform orchestration
- Decide business outcomes
- Implicitly retry or recover
- Mask or suppress failure
- Modify domain state

If error handling determines *what should happen next*, the responsibility has been violated.

---

## Error Handling as Communication, Not Control

Error handling is a **communication mechanism**, not a control mechanism.

- Communication answers: “What failed, and why?”
- Control answers: “What should be done next?”

Control belongs to orchestration and explicit recovery design. Error handling only reports failure.

---

## Determinism and Transparency

Error handling must preserve determinism.

Given the same inputs and execution intent:

- Failures must occur consistently
- Error signals must be predictable
- Failure context must remain intact

Error handling that depends on hidden state or implicit recovery undermines predictability.

---

## Consequences of Boundary Violation

When error handling exceeds its responsibility:

- Failure semantics become ambiguous
- Behavior becomes implicit
- Recovery logic becomes hidden
- Architecture becomes difficult to reason about

Error handling shifts from clarity to control.

---

## Architectural Rule

> Error handling reports failure.  
> Behavior determines response.

This separation is foundational.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-error-handling-placement.md">Next ▶</a>
</p>
