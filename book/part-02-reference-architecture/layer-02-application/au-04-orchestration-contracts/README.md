# AU-04 — Orchestration.Contracts

## Overview

The Orchestration.Contracts Architectural Unit defines the **explicit contracts for multi-step application workflows**.

These contracts describe *what coordinated work the application supports* without defining *how that work is performed*. They are consumed by the Dispatcher and implemented by the Orchestration Architectural Unit.

Orchestration.Contracts exist to make complex behavior **intentional, explicit, and bounded**.

---

## The Role of Orchestration.Contracts

Orchestration.Contracts exist to:

- Define application workflows that exceed simple execution
- Express coordinated intent across multiple operations
- Prevent workflow logic from leaking into handlers
- Preserve clarity between execution and coordination

They answer the question:

> “What workflows does the application support?”

---

## What Belongs in Orchestration.Contracts

This Architectural Unit contains:

- Workflow contracts representing coordinated operations
- Explicit inputs and outputs for those workflows
- Contracts that operate on **domain concepts**, not DTOs

Orchestration.Contracts do not define execution order or logic—only intent.

---

## What Does Not Belong Here

Orchestration.Contracts deliberately exclude:

- Workflow implementation logic
- Domain rule enforcement
- Persistence concerns
- DTO definitions
- Framework-specific behavior

They are **declarations of coordination intent**, nothing more.

---

## What You Will Learn in This AU

The pages in this AU explain:

- What qualifies as a workflow
- When execution escalates to orchestration
- Why orchestration is contract-driven
- How orchestration boundaries protect the application layer

---

## Topics in This AU

- [01 — Workflow Intent](01-workflow-intent.md)
- [02 — Escalation Criteria](02-escalation-criteria.md)
- [03 — Contract Stability](03-contract-stability.md)
- [04 — Boundary Discipline](04-boundary-discipline.md)

---

<p align="center">
  <a href="../au-03-dispatcher/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-05-orchestration/README.md">Next ▶</a>
</p>
