# Transaction Responsibility

## Responsibility

The responsibility of transactions in this architecture is to **ensure that related state changes are committed atomically and consistently, or not at all**.

Transactions protect system correctness by bounding *what must succeed together* and *what must fail together*, without defining behavior, rules, or execution order.

---

## Why This Responsibility Exists

Systems fail.

Failures may occur due to infrastructure faults, concurrency conflicts, partial execution, or unexpected interruption. Without explicit transactional boundaries, partial state changes can corrupt system integrity and make outcomes unpredictable.

Transactions exist to ensure that:

- State changes remain consistent
- Partial updates do not occur
- Failures are contained and recoverable
- Behavior can assume atomic execution

Transactions provide safety, not intent.

---

## What Transactions Are Allowed to Do

Transactions may:

- Define atomic boundaries around state changes
- Ensure consistency across related updates
- Roll back changes on failure
- Isolate execution from partial persistence
- Provide clear commit or abort semantics

Transactions may constrain *how* state is persisted, but they must never influence *what* state changes occur.

---

## What Transactions Must Never Do

Transactions must not:

- Encode business rules
- Decide execution order
- Coordinate workflows
- Determine outcomes
- Replace orchestration
- Mask failure conditions

If transaction boundaries determine behavior semantics, the responsibility has been violated.

---

## Transactions as Consistency, Not Coordination

Transactions provide **consistency guarantees**, not **coordination logic**.

- Consistency answers: “Did all related changes succeed together?”
- Coordination answers: “What should happen next?”

Transactions ensure atomicity; orchestration determines sequence and intent.

---

## Determinism and Predictability

Transactions preserve determinism in the presence of failure.

Given the same inputs and execution intent:

- State changes either fully commit or fully fail
- Partial outcomes do not persist
- Failure semantics remain explicit

Transactions that introduce conditional behavior undermine predictability.

---

## Consequences of Boundary Violation

When transactions exceed their responsibility:

- Business logic becomes implicit
- Execution paths become opaque
- Failure handling becomes ambiguous
- Architecture becomes fragile

Transactions shift from protection to control.

---

## Architectural Rule

> Transactions protect consistency.  
> Behavior defines change.

This separation is foundational.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-transaction-placement.md">Next ▶</a>
</p>
