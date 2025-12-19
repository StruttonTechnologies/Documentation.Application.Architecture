# Infrastructure Layer

## Overview

The Infrastructure layer contains the **technical implementations** that support the application.

It is responsible for *how* capabilities are delivered — not *what* the system does or *why* it does it.

Infrastructure provides concrete mechanisms such as persistence, framework integration, and external system access, while remaining subordinate to the Application and Domain layers.

---

## Infrastructure in This Architecture

In this architecture, Infrastructure is intentionally **passive**.

It does not:

- Define application behavior
- Coordinate workflows
- Enforce business rules
- Shape use cases

Instead, Infrastructure exists to **serve the needs of the Application layer** through explicit contracts.

The Application layer decides *when* something happens.  
Infrastructure defines *how* it happens.

---

## Responsibility Boundaries

The Infrastructure layer is responsible for:

- Implementing persistence mechanisms
- Translating technical exceptions into application-safe errors
- Managing framework and storage concerns
- Executing persistence and transaction mechanics

It is **not responsible** for:

- Business logic
- Use-case orchestration
- Validation rules
- Authorization decisions
- Application flow control

These boundaries are enforced structurally through contracts and project references.

---

## Architectural Units in This Layer

The Infrastructure layer is divided into Architectural Units (AUs), each with a distinct responsibility.

Together, these units describe how technical concerns are implemented without leaking into application behavior.

### Architectural Units

- **[AU-01 — Repository.Contracts](./au-01-repository-contracts/README.md)**  
  Defines persistence capabilities and the explicit commit boundary

- **[AU-02 — Repository](./au-02-repository/README.md)**  
  Implements data access logic while staging changes only

- **[AU-03 — EntityFramework](./au-03-entityframework/README.md)**  
  Encapsulates Entity Framework mechanics and persistence execution

Each AU begins with a high-level overview, followed by focused responsibility pages.

---

## Dependency Direction

All dependencies point **inward**.

- Infrastructure depends on:
  - Frameworks
  - Storage technologies
  - External systems

- Application depends on:
  - Infrastructure **contracts**, not implementations

The Infrastructure layer never depends on Application behavior or Domain rules.

This dependency direction is structural and enforced by the solution layout.

---

## How to Read This Layer

You may read the Architectural Units in order or jump directly to a specific concern.

If you are new to the architecture, begin with **Repository.Contracts**, as it establishes the persistence boundary used by all other Infrastructure units.

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./au-01-repository-contracts/README.md">Next ▶</a>
</p>
