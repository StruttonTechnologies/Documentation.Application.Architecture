# Contract Ownership

## Responsibility

Application DTOs are **owned by the Application layer**.

They define how the application is spoken to and how results are returned. While DTOs may be consumed by multiple entry points, ownership remains singular, explicit, and application-centric.

---

## Why This Responsibility Exists

Without clear ownership, DTOs drift.

They begin reflecting client convenience, infrastructure shape, or domain internals. Over time, this creates coupling and instability, and it becomes unclear what the application actually promises.

Contract Ownership exists to ensure that:

- DTOs reflect application intent, not internal structure
- Entry points adapt to the application’s contracts
- The domain remains protected from representation concerns
- Contract changes are deliberate and reviewable

Ownership prevents the “shared model” problem by establishing a single source of truth for interaction.

---

## Architectural Implications

When DTO ownership is clear:

- DTOs evolve intentionally as application capabilities evolve
- Clients remain insulated from internal refactoring
- The Dispatcher becomes the authoritative interpreter of intent
- The domain stays focused on business meaning rather than external representation

DTOs may be visible across boundaries, but they are not controlled by those boundaries.

---

## What This Responsibility Protects

Contract Ownership protects:

- **Architectural clarity**  
  Contracts represent what the application offers

- **Boundary discipline**  
  Representation does not leak inward

- **Change safety**  
  Contracts evolve intentionally, not by accident

- **Long-term maintainability**  
  DTO sprawl is prevented through explicit ownership

---

## Consequences of Violation

When DTO ownership is unclear:

- Multiple representations emerge for the same intent
- Clients and internal layers become tightly coupled
- Refactoring forces coordinated change
- The application’s contract surface becomes inconsistent

Over time, the system shifts from explicit contracts to emergent, fragile conventions.

---

## Relationship to Other Responsibilities

Contract Ownership supports and reinforces:

- **Boundary Translation**  
  Ownership ensures translation occurs at a controlled boundary

- **Stability Over Time**  
  Stability is only achievable when ownership is explicit

Together, these responsibilities define DTOs as application-owned contracts rather than shared models.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-boundary-translation.md">Next ▶</a>
</p>
