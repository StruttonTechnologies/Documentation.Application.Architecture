# Concurrency Anti-Patterns

## Responsibility

The responsibility of identifying concurrency anti-patterns is to ensure that **mechanisms intended to enable overlapping execution do not introduce non-determinism, hidden coordination, or correctness violations**.

These anti-patterns describe common failure modes where concurrency exceeds its architectural role and undermines system integrity.

---

## Why Anti-Patterns Matter

Concurrency misuse often appears as a performance optimization.

Without clear boundaries, concurrent execution introduces race conditions, timing-dependent behavior, and implicit coordination. These failures are difficult to detect, diagnose, and correct.

Anti-patterns exist to make these risks explicit and prevent architectural erosion.

---

## Concurrency as Control Flow

**Anti-pattern:**  
Using concurrency mechanisms to determine execution order or behavior sequencing.

When concurrency decides *what happens next*, execution becomes timing-dependent and implicit.

Consequences include:

- Hidden sequencing logic
- Non-deterministic outcomes
- Difficult reasoning about behavior

Concurrency must never determine flow.

---

## Concurrency as Business Logic

**Anti-pattern:**  
Allowing concurrent execution to alter business outcomes.

When results depend on timing or interleaving, domain correctness is compromised.

This leads to:

- Race conditions affecting meaning
- Inconsistent state transitions
- Loss of domain authority

Business logic must remain timing-independent.

---

## Concurrency as Implicit Coordination

**Anti-pattern:**  
Using shared state or synchronization primitives as coordination mechanisms.

When coordination is implicit, responsibility becomes unclear and behavior becomes fragile.

This results in:

- Tight coupling between concurrent components
- Hidden dependencies
- Increased cognitive load

Coordination must be explicit and intentional.

---

## Concurrency as Performance Assumption

**Anti-pattern:**  
Designing behavior that assumes parallel execution for correctness.

When behavior requires parallelism, architecture becomes dependent on infrastructure capabilities.

This introduces:

- Environment-dependent correctness
- Reduced portability
- Fragile performance assumptions

Correctness must not depend on performance characteristics.

---

## Concurrency as Error Masking

**Anti-pattern:**  
Using concurrency to hide latency, failure, or contention.

When concurrency masks underlying issues, diagnosis becomes difficult and behavior unpredictable.

This leads to:

- Silent degradation
- Reduced observability
- Deferred failure

Concurrency must not hide problems.

---

## Architectural Rule

> If concurrency changes outcomes,  
> concurrency has exceeded its role.

This rule is absolute.

---

## Architectural Outcome

When concurrency anti-patterns are avoided:

- Behavior remains deterministic
- State remains consistent
- Responsibility remains clear
- Architecture remains robust

Concurrency enables performance without redefining meaning.

---

<p align="center">
  <a href="./03-concurrency-vs-parallelism.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../scalability/README.md">Next ▶</a>
</p>
