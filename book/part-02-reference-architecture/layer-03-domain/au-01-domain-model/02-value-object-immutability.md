# Value Object Immutability

## Responsibility

Value Objects in the Domain Model Architectural Unit are **immutable representations of business concepts**.

Once created, a Value Object does not change. Any modification results in the creation of a new instance that represents a new value.

Immutability ensures that values remain reliable, comparable, and safe to share throughout the system.

---

## Why This Responsibility Exists

Many business concepts are defined by their value, not by identity.

Dates, measurements, classifications, and descriptors do not have lifecycles. They are meaningful only in terms of what they represent at a given moment.

If such concepts are mutable, correctness becomes difficult to reason about. Changes ripple unexpectedly, assumptions break silently, and shared references become a source of defects.

Value Object Immutability exists to ensure that:

- Values represent facts, not evolving state
- Reasoning about business rules remains straightforward
- Domain concepts remain stable and predictable

Immutability removes time and ambiguity from value-based concepts.

---

## Architectural Implications

When value objects are immutable:

- They can be safely shared across entities
- Equality is based on value, not reference
- State transitions are explicit and intentional
- Side effects are eliminated

Value objects become **trustworthy building blocks** within the domain model.

This simplifies both modeling and reasoning about business behavior.

---

## What This Responsibility Protects

Value Object Immutability protects:

- **Model correctness**  
  Values cannot be modified unexpectedly

- **Behavioral predictability**  
  State changes are explicit and observable

- **Invariant enforcement**  
  Validation occurs at creation, not after mutation

- **Conceptual clarity**  
  Values represent facts, not processes

These protections reinforce the reliability of the domain model.

---

## Consequences of Violation

When value objects are mutable:

- Shared state leads to subtle defects
- Equality becomes ambiguous
- Invariants are weakened or bypassed
- Business meaning erodes

Over time, mutable value objects introduce hidden coupling and undermine confidence in the domain model.

---

## Relationship to Other Responsibilities

Value Object Immutability works in concert with:

- **Entity Integrity**  
  Entities rely on stable values to preserve correctness

- **Explicit Invariants**  
  Validation is enforced at creation time

- **Domain Purity**  
  Immutability is most effective in an isolated, dependency-free domain

Together, these responsibilities ensure that the domain model remains safe, expressive, and reliable.

---

<p align="center">
  <a href="./01-entity-integrity.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-explicit-invariants.md">Next ▶</a>
</p>
