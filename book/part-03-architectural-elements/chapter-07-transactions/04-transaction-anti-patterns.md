# Transaction Anti-Patterns

## Responsibility

The responsibility of identifying transaction anti-patterns is to ensure that **transactions remain consistency mechanisms and do not become implicit control flow, orchestration, or business logic**.

These anti-patterns describe common failure modes where transactional boundaries exceed their architectural role and undermine clarity and correctness.

---

## Why Anti-Patterns Matter

Transaction misuse is rarely intentional.

It often begins as a convenience to “make things safe” and gradually becomes a hidden mechanism for sequencing behavior, retrying execution, or encoding business outcomes. Over time, this results in opaque execution paths and fragile systems.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Transactions as Control Flow

**Anti-pattern:**  
Using transaction scope to determine execution order or branching behavior.

When transaction boundaries influence *what happens next*, they silently become control flow mechanisms.

Consequences include:

- Hidden sequencing logic
- Implicit retries
- Unclear responsibility for execution order

Transactions must never determine flow.

---

## Transactions as Business Logic

**Anti-pattern:**  
Encoding business rules or outcome semantics within transactional boundaries.

Transactions protect consistency; they do not determine correctness.

This leads to:

- Business rules becoming implicit
- Outcomes being inferred from commit success
- Domain logic losing authority

Correctness belongs to domain behavior, not transactions.

---

## Transactions as Orchestration

**Anti-pattern:**  
Using a single transaction to coordinate multiple behavioral steps or workflows.

Transactions are not designed to manage sequencing, compensation, or branching logic. When they do, behavior becomes opaque and brittle.

This results in:

- Long-lived transactional scope
- Hidden coupling between steps
- Poor failure recovery semantics

Orchestration must remain explicit.

---

## Transactions as Error Handling

**Anti-pattern:**  
Using transaction rollback as a general error-handling mechanism.

Rollback indicates consistency failure, not behavioral failure. When rollback is used to manage errors broadly, failure semantics become conflated.

This introduces:

- Misleading success or failure signals
- Implicit retries
- Loss of observability

Errors must be handled where behavior occurs.

---

## Transactions as Integration Boundaries

**Anti-pattern:**  
Using transactions to coordinate distributed systems or external interactions.

Transactions cannot reliably span distributed boundaries. When used this way, they introduce blocking, failure amplification, and architectural coupling.

Distributed coordination requires explicit design, not transactional scope.

---

## Architectural Rule

> If transaction boundaries define behavior,  
> transactions have become orchestration.

This rule is absolute.

---

## Architectural Outcome

When transaction anti-patterns are avoided:

- Consistency remains explicit
- Behavior remains intentional
- Failure semantics remain clear
- Architecture remains robust and understandable

Transactions protect correctness without redefining execution.

---

<p align="center">
  <a href="./03-transactions-vs-orchestration.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../error-handling/README.md">Next ▶</a>
</p>
