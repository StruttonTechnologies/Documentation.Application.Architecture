# Transactions vs Orchestration

## Responsibility

The responsibility of distinguishing transactions from orchestration is to ensure that **atomic consistency guarantees are not confused with workflow coordination or behavioral sequencing**.

This boundary preserves clarity by separating *how state changes are committed* from *how behavior is organized and executed*.

---

## Why the Distinction Matters

Transactions and orchestration are often conflated because they both “wrap” execution.

When transactional boundaries are used to coordinate behavior, transactions silently become control flow. This introduces hidden sequencing, implicit retries, and unclear responsibility.

The distinction exists to ensure that:

- Atomicity remains explicit
- Workflows remain intentional
- Failure semantics remain predictable
- Responsibility remains clearly owned

---

## Transactions

Transactions define **consistency boundaries**.

Transactions:

- Group related state changes
- Ensure atomic commit or rollback
- Protect against partial persistence
- Resolve success or failure as a unit

Transactions answer the question:

> “What state changes must succeed or fail together?”

Transactions do not define *what* work is performed or *when* it occurs.

---

## Orchestration

Orchestration defines **behavioral sequencing**.

Orchestration:

- Coordinates steps of execution
- Determines ordering and conditional flow
- Responds to outcomes and failures
- Expresses application intent

Orchestration answers the question:

> “What should happen next?”

Orchestration owns behavior; transactions do not.

---

## The Boundary Between Them

The architectural boundary is strict.

- Orchestration determines execution flow
- Transactions enforce atomicity within that flow
- Orchestration may span multiple transactions
- Transactions must never span multiple orchestration intents

If understanding workflow requires analyzing transactional scope, the boundary has been violated.

---

## Failure Semantics

This distinction preserves clear failure handling.

- Transaction failure means *state was not committed*
- Orchestration failure means *behavior did not complete as intended*

Conflating these concerns leads to retries, compensation, or branching logic hidden inside transactional mechanisms.

---

## Common Boundary Violations

Typical violations include:

- Using transaction scope to determine workflow steps
- Retrying behavior implicitly through transaction rollback
- Encoding sequencing logic in persistence mechanisms
- Treating transaction success as business success

These patterns replace explicit orchestration with implicit control.

---

## Architectural Rule

> Orchestration defines sequence.  
> Transactions define consistency.

This separation is non-negotiable.

---

<p align="center">
  <a href="./02-transaction-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-transaction-anti-patterns.md">Next ▶</a>
</p>
