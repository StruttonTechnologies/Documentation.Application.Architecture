# Transaction Placement

## Responsibility

The responsibility of transaction placement is to ensure that **atomic consistency boundaries are applied at the correct architectural layer without leaking transactional concerns into business behavior**.

Correct placement preserves clarity of intent, isolates failure handling, and prevents transactional mechanics from becoming implicit control flow.

---

## Why Placement Matters

Transactions are powerful and dangerous.

When transaction boundaries are misplaced, they silently influence execution order, hide failure modes, and entangle behavior with persistence mechanics. Placement rules exist to ensure that transactions protect consistency without redefining architecture.

Proper placement ensures that:

- Atomicity is explicit and intentional
- Failure semantics are predictable
- Behavioral logic remains persistence-agnostic
- Responsibility remains clearly owned

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not interact with transactions.

Presentation concerns end at expressing intent. Introducing transactional behavior here couples user interaction to persistence mechanics and creates hidden execution dependencies.

Presentation remains non-transactional.

---

### Application Layer

The Application layer defines **transactional boundaries**.

Responsibilities include:

- Determining which operations must succeed together
- Establishing transactional scope around behavior execution
- Ensuring behavior executes within a single consistency boundary

The Application layer declares *where* a transaction begins and ends. It does not implement transactional mechanics.

---

### Domain Layer

The Domain layer is unaware of transactions.

Domain logic assumes that execution occurs within an appropriate consistency boundary. Introducing transactional concepts here couples business truth to persistence concerns and violates separation of responsibilities.

---

### Infrastructure Layer

The Infrastructure layer implements **transactional mechanics**.

Responsibilities include:

- Providing transaction implementations
- Managing commit and rollback
- Handling concurrency and isolation
- Integrating with persistence mechanisms

Infrastructure enforces transactions; it does not define their scope.

---

## Transactions at Architectural Boundaries

Transactions belong **around behavior execution**, not within it.

Architecturally correct placement ensures that:

- Transactions wrap complete behavioral intent
- Partial execution cannot persist
- Failure handling remains explicit
- Behavior does not manage persistence mechanics

Transactions must never be nested arbitrarily or introduced implicitly.

---

## Consequences of Improper Placement

When transactions are misplaced:

- Business logic becomes persistence-aware
- Failure handling becomes opaque
- Execution paths become difficult to trace
- Architecture becomes brittle

Misplaced transactions transform safety mechanisms into sources of risk.

---

## Architectural Rule

> Transactions are declared by the Application layer  
> and enforced by the Infrastructure layer.

This rule governs all transaction placement decisions.

---

<p align="center">
  <a href="./01-transaction-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-transactions-vs-orchestration.md">Next ▶</a>
</p>
