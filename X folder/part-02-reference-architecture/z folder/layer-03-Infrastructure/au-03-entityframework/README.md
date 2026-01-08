# AU-03 — EntityFramework

## Overview

The EntityFramework Architectural Unit contains the **framework-specific implementation** of persistence concerns.

It encapsulates Entity Framework, database contexts, and persistence execution mechanics, ensuring that framework behavior does not leak into application logic.

In this architecture, Entity Framework is a **detail**, not a dependency.

---

## The Role of EntityFramework

EntityFramework exists to:

- Implement persistence mechanisms
- Execute commits and transactions
- Translate framework failures into application-safe errors
- Isolate Entity Framework from the rest of the system

It answers the question:

> “How is persistence actually executed?”

—not—

> “When should persistence occur?”  
> “What business rules apply?”  
> “What workflow should run?”

---

## What Belongs in EntityFramework

This Architectural Unit contains:

- DbContext implementations
- Entity configurations and mappings
- Unit of Work implementations
- Framework-specific exception handling
- Transaction and persistence execution logic

EntityFramework may depend on:
- Entity Framework Core
- Database providers
- Infrastructure utilities

---

## What Does Not Belong Here

EntityFramework deliberately excludes:

- Application logic
- Workflow coordination
- Validation or authorization rules
- Business invariants
- Use-case decisions

It executes decisions made elsewhere.

---

## What You Will Learn in This AU

The pages in this AU explain:

- Why framework isolation is critical
- How persistence execution is centralized
- How transactions and failures are handled safely

---

## Topics in This AU

- [01 — Framework Encapsulation](01-framework-encapsulation.md)
- [02 — Persistence Execution](02-persistence-execution.md)
- [03 — Transaction and Failure Handling](03-transaction-and-failure-handling.md)

---

<p align="center">
  <a href="../au-02-repository/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-framework-encapsulation.md">Next ▶</a>
</p>
