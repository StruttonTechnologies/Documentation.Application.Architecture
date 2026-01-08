# Persistence Execution

## Responsibility

EntityFramework is responsible for **executing persistence operations**.

This includes committing staged changes, coordinating database interaction, and ensuring atomic execution.

Persistence execution occurs through the Unit of Work implementation.

---

## Why This Responsibility Exists

Repositories stage changes, but they do not finalize them.

Execution must occur in a single, controlled location to ensure correctness and predictability.

Centralizing persistence execution ensures that:

- Commit behavior is consistent
- Transactional boundaries are enforced
- Persistence failures are handled uniformly

---

## Architectural Implications

When persistence execution is centralized:

- Workflows define transactional scope
- Simple operations remain lightweight
- Persistence behavior is explicit and traceable

The system has a **single point of persistence finalization**.

---

## What This Responsibility Protects

Persistence Execution protects:

- **Transactional integrity**
- **Consistency**
- **Operational safety**

---

## Consequences of Violation

When persistence execution is scattered:

- Partial commits occur
- Transactions fragment
- Failure recovery becomes unpredictable

Over time, persistence correctness becomes accidental.

---

<p align="center">
  <a href="./01-framework-encapsulation.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-transaction-and-failure-handling.md">Next ▶</a>
</p>
