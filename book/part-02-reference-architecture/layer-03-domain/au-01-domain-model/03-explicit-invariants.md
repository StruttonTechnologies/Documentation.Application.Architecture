# Explicit Invariants

## Responsibility

The Domain Model Architectural Unit is responsible for **explicitly defining and enforcing business invariants**.

Invariants are rules that must always hold true for the domain to remain valid. They define the conditions under which business concepts may exist and change.

Explicit Invariants ensure that invalid state cannot be represented within the domain model.

---

## Why This Responsibility Exists

Business rules are not optional constraints.  
They define correctness.

If invariants are implicit, undocumented, or enforced outside the domain model, they become fragile. Different parts of the system begin to interpret rules differently, and invalid state slips through unnoticed.

Explicit Invariants exist to ensure that:

- Business rules are enforced at the point of truth
- Validity is preserved regardless of usage context
- Domain correctness does not depend on external discipline

Rules that define the business must live with the concepts they govern.

---

## Architectural Implications

When invariants are explicit and enforced within the domain:

- Invalid state cannot be constructed
- State transitions are intentional and constrained
- Validation logic is centralized and discoverable
- Higher layers can trust the domain model

The domain becomes **self-protecting**, rather than dependent on external validation.

---

## What This Responsibility Protects

Explicit Invariants protect:

- **Business correctness**  
  Invalid or contradictory states are prevented

- **Model integrity**  
  Rules remain coupled to the concepts they define

- **Consistency across use cases**  
  Behavior does not vary by execution path

- **Architectural clarity**  
  Responsibility for correctness is unambiguous

These protections preserve the domain as the single source of business truth.

---

## Consequences of Violation

When invariants are implicit or enforced elsewhere:

- Rules are duplicated across layers
- Invalid state is created and propagated
- Bugs emerge that are difficult to diagnose
- Business meaning erodes over time

Eventually, the domain becomes permissive rather than authoritative, and correctness becomes a coordination problem instead of a modeling concern.

---

## Relationship to Other Responsibilities

Explicit Invariants depend on and reinforce:

- **Entity Integrity**  
  Invariants govern how entities may change

- **Value Object Immutability**  
  Values are validated once and trusted thereafter

- **Domain Purity**  
  Invariants remain meaningful only when free from technical concerns

Together, these responsibilities ensure that the domain model remains correct by construction.

---

<p align="center">
  <a href="./02-value-object-immutability.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-domain-purity.md">Next ▶</a>
</p>
