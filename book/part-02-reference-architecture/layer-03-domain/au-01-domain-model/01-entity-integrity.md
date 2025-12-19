# Entity Integrity

## Responsibility

Entities in the Domain Model Architectural Unit are responsible for **preserving identity and enforcing business invariants** over their lifetime.

An entity is not defined by its data alone, but by its continuity and the rules that govern how it may change.

Entity Integrity ensures that business concepts remain valid regardless of how or where they are used.

---

## Why This Responsibility Exists

Business rules do not exist at the edges of a system.  
They exist at its core.

If entities are treated as passive data structures, responsibility for enforcing correctness shifts outward—to application logic, delivery layers, or persistence mechanisms. Over time, this leads to duplication, inconsistency, and erosion of business meaning.

Entity Integrity exists to ensure that:

- Business rules are enforced at the point of truth
- Invalid state cannot be represented or persisted
- Changes to business concepts remain intentional

Entities protect the business model from misuse, not the other way around.

---

## Architectural Implications

When entity integrity is preserved:

- Entities guard their own validity
- State transitions are intentional and constrained
- Business rules are centralized and discoverable
- Application and infrastructure layers rely on the model, rather than compensating for it

Entities become **behavioral objects**, not data carriers.

This allows higher layers to focus on coordination rather than correction.

---

## What This Responsibility Protects

Entity Integrity protects:

- **Business correctness**  
  Invalid or contradictory states cannot exist

- **Model coherence**  
  Rules are expressed where the concepts live

- **Change safety**  
  Business rules evolve in one place

- **Architectural clarity**  
  Responsibilities remain properly aligned

These protections preserve the domain as the authoritative source of truth.

---

## Consequences of Violation

When entity integrity is compromised:

- Business rules are scattered across layers
- Invalid states are persisted and propagated
- Bugs emerge that are difficult to trace
- The domain loses expressive power

Over time, the domain model degenerates into a collection of data structures, and the system’s behavior becomes harder to reason about and change.

---

## Relationship to Other Responsibilities

Entity Integrity supports and reinforces:

- **Value Object Immutability**  
  Entities rely on stable, correct value representations

- **Explicit Invariants**  
  Rules governing validity are expressed directly in the model

- **Domain Purity**  
  Integrity is only meaningful when the domain is isolated from technical concerns

Together, these responsibilities ensure that the Domain Model remains expressive, trustworthy, and durable.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-value-object-immutability.md">Next ▶</a>
</p>
