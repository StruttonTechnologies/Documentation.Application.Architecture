# Concurrency vs Parallelism

## Responsibility

The responsibility of distinguishing concurrency from parallelism is to ensure that **overlapping execution intent is not confused with simultaneous physical execution**.

This boundary preserves architectural clarity by separating *how work is structured* from *how work is executed by the system*.

---

## Why the Distinction Matters

Concurrency and parallelism are often used interchangeably, but they address different concerns.

When parallel execution is assumed as a behavioral requirement, system correctness becomes dependent on hardware, scheduling, or infrastructure capabilities. The distinction exists to ensure that architectural intent remains independent of execution environment.

This boundary ensures that:

- Behavior remains deterministic
- Execution intent remains explicit
- Architecture remains portable
- Performance characteristics do not redefine correctness

---

## Concurrency

Concurrency defines **overlapping execution intent**.

Concurrency:

- Describes how work is organized
- Allows multiple units of work to be in progress
- Does not require simultaneous execution
- Preserves logical ordering and correctness

Concurrency answers the question:

> “What work may be in progress at the same time?”

Concurrency is an architectural concern.

---

## Parallelism

Parallelism defines **simultaneous execution**.

Parallelism:

- Describes how work is executed physically
- Depends on available resources
- Is influenced by scheduling and hardware
- Is an optimization, not a requirement

Parallelism answers the question:

> “How many things are executing at the same instant?”

Parallelism is an infrastructure concern.

---

## The Boundary Between Them

The architectural boundary is strict.

- Concurrency defines intent
- Parallelism provides execution capability
- Concurrency must not assume parallel execution
- Parallelism must not alter behavioral meaning

If correctness depends on parallel execution, the boundary has been violated.

---

## Determinism and Portability

This distinction preserves determinism and portability.

- Concurrency expresses safe overlap
- Parallelism may vary across environments
- Behavior must remain correct without parallelism
- Performance optimization must not redefine outcomes

Systems must behave correctly even when parallel execution is constrained or unavailable.

---

## Common Boundary Violations

Typical violations include:

- Designing behavior that assumes simultaneous execution
- Encoding performance assumptions into business logic
- Treating parallelism as a correctness requirement
- Allowing execution environment to influence outcomes

These patterns couple architecture to infrastructure.

---

## Architectural Rule

> Concurrency defines intent.  
> Parallelism provides execution.

This separation is non-negotiable.

---

<p align="center">
  <a href="./02-concurrency-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-concurrency-anti-patterns.md">Next ▶</a>
</p>
