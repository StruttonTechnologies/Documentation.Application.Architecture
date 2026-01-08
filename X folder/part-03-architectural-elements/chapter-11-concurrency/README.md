# Concurrency

## Overview

Concurrency defines the architectural responsibility for **allowing multiple units of work to execute simultaneously while preserving correctness, intent, and predictable outcomes**.

Within this architecture, concurrency exists to improve throughput and responsiveness without introducing race conditions, hidden coupling, or non-deterministic behavior.

Concurrency answers the question:

> “What work may proceed at the same time without violating correctness?”

It does not answer:

> “What behavior should occur?”  
> “What outcome should be chosen?”  
> “How should work be coordinated across responsibilities?”

---

## The Role of Concurrency in the Architecture

Concurrency exists to:

- Enable parallel execution of independent work
- Improve utilization of system resources
- Reduce latency under load
- Preserve responsiveness at scale
- Allow safe overlap of execution

Concurrency enables performance; it does not define meaning.

---

## Architectural Constraints

Concurrency is governed by strict architectural constraints to prevent responsibility erosion and unpredictable behavior.

Concurrency must:

- Be explicit and intentional
- Preserve domain invariants
- Maintain deterministic outcomes
- Respect transactional and consistency boundaries
- Remain observable and explainable

Concurrency must not:

- Alter business rules
- Introduce implicit coordination
- Mask race conditions
- Redefine execution intent
- Replace explicit orchestration

When concurrency changes outcomes, the boundary has been violated.

---

## Concurrency and Responsibility Boundaries

Concurrency operates **within execution**, not as a driver of behavior.

Architecturally:

- Behavior defines what work exists
- Transactions protect consistency
- Resilience contains failure
- Concurrency governs simultaneous execution

Each concern remains distinct. Concurrency must not absorb the responsibilities of others.

---

## Concurrency and Change

Concurrency exists to manage **execution overlap**, not **business evolution**.

Correct concurrency design ensures that changes in load, timing, or parallelism do not:

- Alter business outcomes
- Introduce hidden execution paths
- Require defensive logic across layers

Concurrency preserves performance while maintaining architectural clarity.

---

## Pages in This Section

- **[01 — Concurrency Responsibility](./01-concurrency-responsibility.md)**  
  Defines concurrency as an architectural responsibility and establishes its scope

- **[02 — Concurrency Placement](./02-concurrency-placement.md)**  
  Explains where concurrency belongs in the architecture and where it cannot exist

- **[03 — Concurrency vs Parallelism](./03-concurrency-vs-parallelism.md)**  
  Clarifies the conceptual boundary between overlapping execution and simultaneous processing

- **[04 — Concurrency Anti-Patterns](./04-concurrency-anti-patterns.md)**  
  Identifies common architectural violations involving concurrency misuse

---

<p align="center">
  <a href="../resilience/04-resilience-anti-patterns.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-concurrency-responsibility.md">Next ▶</a>
</p>
