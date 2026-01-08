# Scalability Anti-Patterns

## Responsibility

The responsibility of identifying scalability anti-patterns is to ensure that **capacity growth mechanisms do not silently alter behavior, correctness, or architectural intent**.

These anti-patterns describe common failure modes where scalability concerns exceed their proper scope and introduce instability or meaning drift.

---

## Why Anti-Patterns Matter

Scalability issues often emerge gradually.

Initial success leads to growth, growth introduces pressure, and pressure encourages shortcuts. Without clear boundaries, scalability mechanisms become entangled with behavior, changing outcomes under load.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Scalability as Business Logic

**Anti-pattern:**  
Altering business behavior based on system load or capacity.

When outcomes differ because the system is under stress, scalability has become business logic.

Consequences include:

- Load-dependent semantics
- Inconsistent user experience
- Loss of domain authority

Business meaning must remain independent of capacity.

---

## Scalability as Control Flow

**Anti-pattern:**  
Using load or capacity signals to drive execution paths.

When the system changes *what it does* under load rather than *how much it can do*, behavior becomes implicit and unpredictable.

This results in:

- Hidden branching logic
- Timing-dependent outcomes
- Reduced traceability

Control flow must remain explicit.

---

## Scalability as Masking

**Anti-pattern:**  
Masking architectural flaws through scaling.

Scaling cannot compensate for incorrect design, missing boundaries, or flawed assumptions. When scaling is used to hide problems, failure is deferred rather than resolved.

This introduces:

- Increased operational cost
- Delayed failure
- Harder diagnosis

Scalability must not conceal defects.

---

## Scalability as Performance Tuning

**Anti-pattern:**  
Treating performance optimization as the primary scalability strategy.

Performance gains may delay capacity limits, but they do not replace scalable design. When optimization is mistaken for scalability, growth eventually stalls.

This leads to:

- Fragile systems under growth
- Constant tuning pressure
- Unpredictable behavior

Capacity and speed are distinct concerns.

---

## Scalability as Environment Dependency

**Anti-pattern:**  
Allowing behavior to vary across environments due to scaling differences.

When correctness depends on infrastructure size or capacity, architecture becomes environment-specific and brittle.

This results in:

- Non-portable behavior
- Testing complexity
- Inconsistent outcomes

Behavior must remain consistent regardless of scale.

---

## Architectural Rule

> If scalability changes behavior,  
> scalability has exceeded its role.

This rule is absolute.

---

## Architectural Outcome

When scalability anti-patterns are avoided:

- Growth remains safe and predictable
- Behavior remains consistent
- Responsibility remains clear
- Architecture remains resilient under demand

Scalability enables growth without redefining meaning.

---

<p align="center">
  <a href="./03-scalability-vs-performance.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../deployment/README.md">Next ▶</a>
</p>
