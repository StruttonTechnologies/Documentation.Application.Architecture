# Data Access Only

## Responsibility

Repositories are responsible for **data access only**.

They retrieve, add, update, and remove data according to persistence contracts, without embedding application behavior or business intent.

---

## Why This Responsibility Exists

Data access is a technical concern.

When repositories include business logic or workflow decisions, they become tightly coupled to application behavior and difficult to reason about or reuse.

Restricting repositories to data access ensures that:

- Business rules remain in the Domain
- Workflows remain in Orchestration
- Application behavior remains explicit

---

## Architectural Implications

When repositories focus solely on data access:

- Persistence logic is predictable
- Behavior remains centralized in the Application layer
- Repositories can be replaced or refactored safely

Repositories act as **technical adapters**, not application services.

---

## What This Responsibility Protects

Data Access Only protects:

- **Layer separation**
- **Architectural clarity**
- **Long-term maintainability**

---

## Consequences of Violation

When repositories contain behavior:

- Business rules become scattered
- Workflow logic becomes implicit
- Refactoring becomes risky

Over time, repositories evolve into services, and architectural boundaries erode.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-no-commit-no-coordination.md">Next ▶</a>
</p>
