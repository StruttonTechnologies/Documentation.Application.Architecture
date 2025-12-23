# Concurrency Placement

## Responsibility

The responsibility of concurrency placement is to ensure that **simultaneous execution is applied at the correct architectural boundary without leaking concurrency concerns into business behavior or domain logic**.

Correct placement preserves determinism, protects correctness, and prevents concurrency from becoming an implicit source of control flow.

---

## Why Placement Matters

Concurrency is powerful and subtle.

When concurrency concerns are embedded directly into behavioral logic, execution order becomes implicit, state assumptions break down, and responsibility boundaries erode. Placement rules exist to ensure that concurrency remains intentional, observable, and safe.

Proper placement ensures that:

- Overlapping execution is explicit
- Shared state remains protected
- Behavioral intent remains clear
- Outcomes remain predictable

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not manage concurrency.

Presentation concerns may initiate multiple requests or interactions, but they must not coordinate or reason about concurrent execution. Introducing concurrency logic here couples user interaction to execution mechanics.

Presentation expresses intent; it does not manage overlap.

---

### Application Layer

The Application layer defines **concurrency intent**.

Responsibilities include:

- Declaring which units of work may execute concurrently
- Establishing boundaries for parallel execution
- Coordinating concurrent intent without embedding execution mechanics

The Application layer decides *where* concurrency is allowed, not *how* it is implemented.

---

### Domain Layer

The Domain layer is unaware of concurrency.

Domain logic assumes that execution occurs in a manner that preserves invariants and correctness. Introducing concurrency concerns here couples business truth to execution timing and violates architectural independence.

Domain behavior must remain valid regardless of overlap.

---

### Infrastructure Layer

The Infrastructure layer implements **concurrency mechanisms**.

Responsibilities include:

- Managing threads, tasks, or execution resources
- Enforcing synchronization and isolation
- Preventing race conditions and state corruption
- Applying concurrency limits or scheduling policies

Infrastructure enforces concurrency; it does not decide intent.

---

## Concurrency at Architectural Boundaries

Concurrency belongs **around execution boundaries**, not within business logic.

Architecturally correct placement ensures that:

- Concurrency is applied consistently
- Behavioral logic remains unchanged
- Overlap remains observable
- Responsibility remains clear

Concurrency must never be implicit or hidden.

---

## Consequences of Improper Placement

When concurrency is misplaced:

- Behavior becomes timing-dependent
- State corruption becomes possible
- Execution paths become implicit
- Architecture becomes fragile

Misplaced concurrency transforms performance optimization into correctness risk.

---

## Architectural Rule

> Concurrency intent is declared by the Application layer  
> and enforced by the Infrastructure layer.

This rule governs all concurrency placement decisions.

---

<p align="center">
  <a href="./01-concurrency-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-concurrency-vs-parallelism.md">Next ▶</a>
</p>
