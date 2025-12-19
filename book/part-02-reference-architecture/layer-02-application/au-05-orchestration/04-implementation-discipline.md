****# Implementation Discipline

## Responsibility

Orchestration enforces **strict implementation discipline**.

Workflow implementations remain focused on coordination, sequencing, and transactional control—never on business rules, validation, or infrastructure mechanics.

---

## Why This Responsibility Exists

Without discipline, orchestration becomes a dumping ground.

Logic accumulates, responsibilities blur, and workflows become difficult to change. Discipline ensures orchestration remains a **coordination layer**, not a second domain.

---

## Architectural Implications

When orchestration is disciplined:

- Workflows remain readable
- Responsibilities remain clear
- Refactoring remains safe
- Architecture remains intentional

---

## Consequences of Violation

Undisciplined orchestration leads to:

- Bloated workflows
- Hidden business logic
- Architectural drift

Eventually, the Application layer loses its shape.

---

## Relationship to Other Responsibilities

Implementation Discipline reinforces:

- **Workflow Intent** (Orchestration.Contracts)
- **Handler Scope and Discipline**
- **Domain Coordination**

Together, these responsibilities complete the Application layer’s execution model.

---

<p align="center">
  <a href="./03-transactional-boundaries.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../../layer-03-domain/README.md">Next ▶</a>
</p>
