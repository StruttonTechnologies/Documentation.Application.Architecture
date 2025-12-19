# Domain Coordination

## Responsibility

Orchestration is responsible for **coordinating interactions between domain entities and value objects**.

It sequences domain behavior without embedding business rules or invariants. Orchestration asks the domain to act; it does not decide *how* the domain behaves.

---

## Why This Responsibility Exists

Domain models should enforce business meaning, not coordination flow.

When coordination logic leaks into domain entities, they become context-aware and brittle. Orchestration exists to keep domain models focused on correctness while handling cross-entity interaction externally.

---

## Architectural Implications

When coordination is externalized:

- Domain entities remain cohesive
- Business rules remain enforceable
- Cross-entity behavior is explicit
- Testing remains focused and isolated

Coordination becomes **visible**, not hidden.

---

## What This Responsibility Protects

Domain Coordination protects:

- **Domain purity**  
  Entities enforce rules, not workflows

- **Reusability**  
  Domain behavior can be composed safely

- **Architectural clarity**  
  Responsibilities remain easy to locate

---

## Consequences of Violation

When coordination is embedded in the domain:

- Entities become tightly coupled
- Business rules blur with workflow logic
- Change ripples unpredictably

Eventually, the domain becomes difficult to evolve or reuse.

---

<p align="center">
  <a href="./01-workflow-execution.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-transactional-boundaries.md">Next ▶</a>
</p>
