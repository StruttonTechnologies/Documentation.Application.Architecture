# AU-02 — Repository

## Overview

The Repository Architectural Unit contains the **concrete implementations** of persistence contracts.

Repositories provide access to stored data and stage changes on behalf of the Application layer. They do not define transactional boundaries, coordinate workflows, or contain application behavior.

In this architecture, repositories are **mechanisms**, not decision-makers.

---

## The Role of Repositories

Repositories exist to:

- Implement persistence contracts
- Encapsulate data access logic
- Isolate storage technology
- Stage changes for later commitment

They answer the question:

> “How is data accessed and modified?”

—not—

> “When should changes be persisted?”  
> “Why is this operation occurring?”  
> “What workflow should run?”

---

## What Belongs in Repositories

This Architectural Unit contains:

- Concrete repository implementations
- Query logic and persistence operations
- Data access concerns specific to storage technology
- Exception translation for persistence operations

Repositories may depend on:
- Entity Framework
- Database contexts
- Infrastructure utilities

---

## What Does Not Belong Here

Repositories deliberately exclude:

- Transaction management
- Persistence commits
- Workflow coordination
- Validation logic
- Authorization rules
- Business decisions

Repositories **stage changes only**.  
They never finalize persistence.

---

## What You Will Learn in This AU

The pages in this AU explain:

- Why repositories are limited to data access
- Why repositories do not commit or coordinate
- How repositories translate technical failures safely

Together, these responsibilities ensure repositories remain focused, predictable, and replaceable.

---

## Topics in This AU

- [01 — Data Access Only](01-data-access-only.md)
- [02 — No Commit, No Coordination](02-no-commit-no-coordination.md)
- [03 — Exception Translation](03-exception-translation.md)

---

<p align="center">
  <a href="../au-01-repository-contracts/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-data-access-only.md">Next ▶</a>
</p>
