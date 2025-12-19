# Entry Point Neutrality

## Responsibility

Dispatcher.Contracts are responsible for maintaining **entry point neutrality** across the application.

All entry points—present and future—express intent using the same application contracts. No entry point is privileged, specialized, or allowed to shape application behavior through alternative mechanisms.

Entry Point Neutrality ensures that *how the application is entered* does not affect *how the application behaves*.

---

## Why This Responsibility Exists

Applications rarely have a single entry point forever.

Over time, systems grow to include additional clients, integrations, background processes, or external consumers. If each entry point introduces its own execution path or contract shape, behavior fragments and consistency erodes.

Entry Point Neutrality exists to ensure that:

- All callers speak the same intent language
- Behavior remains consistent regardless of entry point
- New entry points can be added without architectural change
- Execution paths remain centralized and observable

The application should behave the same way no matter who is asking.

---

## Architectural Implications

When entry point neutrality is enforced:

- APIs, frontends, and future clients use identical intent contracts
- The Dispatcher remains the single execution gateway
- Validation, routing, and orchestration remain centralized
- No entry point gains special access or behavior

Entry points become **delivery mechanisms**, not behavioral authorities.

This preserves the application as a cohesive system rather than a collection of access paths.

---

## What This Responsibility Protects

Entry Point Neutrality protects:

- **Behavioral consistency**  
  All callers receive the same outcomes for the same intent

- **Architectural discipline**  
  New entry points cannot bypass established boundaries

- **Future extensibility**  
  Additional clients can be introduced safely

- **Operational confidence**  
  Execution flow remains predictable and auditable

These protections prevent architectural fragmentation as the system grows.

---

## Consequences of Violation

When entry point neutrality is compromised:

- Different callers trigger different behavior
- Execution paths multiply and diverge
- Validation and authorization become inconsistent
- The application becomes difficult to reason about

Over time, the system evolves into multiple applications sharing the same codebase rather than a single coherent application.

---

## Relationship to Other Responsibilities

Entry Point Neutrality depends on and reinforces:

- **Explicit Intent**  
  All callers must express intent in the same way

- **Contract Stability**  
  Neutrality requires durable, shared contracts

- **Dependency Direction**  
  Entry points depend inward on contracts, not implementations

Together, these responsibilities ensure that Dispatcher.Contracts define a **single, neutral language of application intent**.

---

<p align="center">
  <a href="./03-dependency-direction.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-03-dispatcher/README.md">Next ▶</a>
</p>
