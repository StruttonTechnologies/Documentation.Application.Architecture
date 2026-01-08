# AU-02 — Dispatcher.Contracts

## Overview

The Dispatcher.Contracts Architectural Unit defines the **explicit application contracts** used to express intent to the system.

These contracts describe *what the application can do* without defining *how it does it*. They are consumed by the Dispatcher and referenced by entry points such as APIs and clients.

In this architecture, Dispatcher.Contracts represent the **formal boundary between intent and execution**.

---

## The Role of Dispatcher.Contracts

Dispatcher.Contracts exist to define **application intent using CQRS-style Commands and Queries**.

Each contract represents a specific operation the application understands and is willing to process. These contracts describe *what is being requested*, not *how it is fulfilled*.

Commands and Queries are implemented using MediatR, but the architectural responsibility of this unit is independent of any specific library or framework.

Dispatcher.Contracts answer the question:

> “What Commands and Queries does the application support?”

---

## Relationship to CQRS

This architecture adopts **CQRS terminology** to clearly distinguish between:

- **Commands** — requests that express intent to change application state
- **Queries** — requests that express intent to retrieve information

Dispatcher.Contracts define these Commands and Queries explicitly.

CQRS is used here as a **clarifying pattern**, not as a mandate for physical separation of read and write models. Commands and Queries may share infrastructure, storage, or execution paths as appropriate.

The architectural goal is **clarity of intent**, not complexity.

---

## What Belongs in Dispatcher.Contracts

This Architectural Unit contains:

- **Command contracts**  
  CQRS-style commands that express intent to change application state

- **Query contracts**  
  CQRS-style queries that express intent to retrieve information

These contracts reference **Application DTOs** and are handled by the Dispatcher.

They define the application’s *capabilities*, not its implementation.

---

## What Does Not Belong Here

Dispatcher.Contracts deliberately exclude:

- Business rules
- Execution logic
- Domain entities or value objects
- Infrastructure concerns
- Framework-specific behavior

They are **pure declarations of intent**, nothing more.

---

## What You Will Learn in This AU

The pages in this AU explain:

- Why application intent is expressed explicitly as Commands and Queries
- How contracts preserve architectural direction
- Why intent contracts are stable while implementations evolve
- How a single set of contracts enables multiple entry points

This AU defines *what the application offers*, not *how it operates*.

---

## Topics in This AU

- [01 — Explicit Intent](01-explicit-intent.md)
- [02 — Contract Stability](02-contract-stability.md)
- [03 — Dependency Direction](03-dependency-direction.md)
- [04 — Entry Point Neutrality](04-entry-point-neutrality.md)

---

<p align="center">
  <a href="../au-01-application-dtos/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-03-dispatcher/README.md">Next ▶</a>
</p>
