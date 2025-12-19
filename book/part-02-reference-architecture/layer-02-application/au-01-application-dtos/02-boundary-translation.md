# Boundary Translation

## Responsibility

Application DTOs define the **translation boundary** between external representations and domain concepts.

DTOs are translated into domain entities and value objects within the Dispatcher. DTOs themselves are not used as working state inside the system.

Because DTOs are immutable records, intent is fixed at the boundary and cannot be altered during execution.

---

## Why This Responsibility Exists

External representations change frequently.  
Domain concepts should not.

If DTOs cross into the domain, representation concerns leak inward and the domain becomes shaped by external requirements. Over time, business meaning is diluted by transport-driven structure.

Boundary Translation exists to ensure that:

- The domain remains independent of client representation
- Mapping is explicit and reviewable
- External change is absorbed at a controlled boundary
- Intent is interpreted once, consistently, and predictably

---

## Architectural Implications

When translation is explicit:

- The Dispatcher becomes the single interpretation point for intent
- Domain purity is preserved
- Execution paths remain controlled and observable
- Mapping remains intentional rather than automatic or implicit

Translation is not a convenience; it is a boundary enforcement mechanism.

---

## What This Responsibility Protects

Boundary Translation protects:

- **Domain purity**  
  Domain concepts remain free from representation concerns

- **Architectural clarity**  
  The place where intent becomes domain interaction is explicit

- **Execution consistency**  
  Intent is interpreted uniformly across entry points

- **Change resilience**  
  External representation can evolve without destabilizing the core

---

## Consequences of Violation

When DTOs are allowed to leak inward:

- Domain modeling becomes representation-driven
- Changes at the edge force changes at the core
- Mapping becomes scattered and inconsistent
- Architectural boundaries weaken over time

Eventually, the domain becomes a reflection of the system’s delivery mechanisms rather than the business.

---

## Relationship to Other Responsibilities

Boundary Translation depends on and reinforces:

- **Contract Ownership**  
  Ownership defines where translation responsibility lives

- **Stability Over Time**  
  Stable DTOs are meaningful only when translation is controlled

Together, these responsibilities preserve a clear separation between representation and business meaning.

---

<p align="center">
  <a href="./01-contract-ownership.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-stability-over-time.md">Next ▶</a>
</p>
