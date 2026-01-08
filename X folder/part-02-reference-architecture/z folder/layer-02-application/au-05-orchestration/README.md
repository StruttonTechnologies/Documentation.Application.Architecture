# AU-05 — Orchestration

## Overview

The Orchestration Architectural Unit contains the **implementation of application workflows**.

Orchestration executes the workflows defined by Orchestration.Contracts. It coordinates multiple steps, domain interactions, and persistence operations without owning business rules or execution entry points.

Orchestration exists to **manage complexity without spreading it**.

---

## The Role of Orchestration

Orchestration exists to:

- Implement workflow contracts explicitly
- Coordinate multi-step application behavior
- Sequence domain interactions intentionally
- Manage transactional boundaries
- Keep handlers and domain models focused

Orchestration is **where workflows live**, not where intent is defined.

---

## What Belongs in Orchestration

This Architectural Unit contains:

- Workflow implementations
- Coordination logic across domain entities
- Sequencing and conditional execution
- Transaction boundary management

Orchestration operates on **domain entities and value objects**, not DTOs.

---

## What Does Not Belong Here

Orchestration deliberately excludes:

- Entry point logic
- Application-level validation
- Business rule enforcement
- DTO translation
- Infrastructure implementations

It coordinates behavior; it does not define it.

---

## What You Will Learn in This AU

The pages in this AU explain:

- How workflows are executed safely
- How orchestration coordinates domain behavior
- Where transactional boundaries belong
- How orchestration remains disciplined and bounded

---

## Topics in This AU

- [01 — Workflow Execution](01-workflow-execution.md)
- [02 — Domain Coordination](02-domain-coordination.md)
- [03 — Transactional Boundaries](03-transactional-boundaries.md)
- [04 — Implementation Discipline](04-implementation-discipline.md)

---

<p align="center">
  <a href="../au-04-orchestration-contracts/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../../layer-03-domain/README.md">Next ▶</a>
</p>
