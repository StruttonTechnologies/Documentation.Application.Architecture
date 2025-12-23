# Resilience Placement

## Responsibility

The responsibility of resilience placement is to ensure that **failure containment mechanisms are applied at appropriate architectural boundaries without leaking resilience logic into business behavior**.

Correct placement preserves intent clarity, prevents hidden behavior changes, and ensures that resilience remains a protective concern rather than a behavioral one.

---

## Why Placement Matters

Resilience is inherently cross-cutting, but it must not be pervasive.

When resilience mechanisms are embedded directly into behavioral logic, failure handling becomes implicit, outcomes become environment-dependent, and responsibility boundaries erode. Placement rules exist to ensure that resilience remains intentional, observable, and predictable.

Proper placement ensures that:

- Failure containment is explicit
- Degradation paths are intentional
- Behavioral logic remains stable
- Responsibility remains centralized

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not own resilience.

Presentation concerns may reflect degraded availability or partial capability to the user, but they must not implement resilience logic or determine degradation behavior.

Presentation communicates state; it does not manage failure.

---

### Application Layer

The Application layer defines **resilience intent**.

Responsibilities include:

- Declaring which interactions must tolerate failure
- Defining acceptable degradation boundaries
- Establishing resilience scope around execution

The Application layer decides *where* resilience applies, not *how* it is implemented.

---

### Domain Layer

The Domain layer is unaware of resilience concerns.

Domain logic represents business truth and correctness. Introducing resilience here couples domain meaning to infrastructure instability and violates architectural independence.

Domain behavior must remain stable regardless of failure conditions.

---

### Infrastructure Layer

The Infrastructure layer implements **resilience mechanisms**.

Responsibilities include:

- Enforcing failure isolation
- Applying timeouts, limits, or isolation
- Managing interaction with unstable dependencies
- Supporting controlled degradation

Infrastructure enforces resilience; it does not decide intent.

---

## Resilience at Architectural Boundaries

Resilience belongs **around execution boundaries**, not within domain behavior.

Architecturally correct placement ensures that:

- Failure containment is applied consistently
- Behavioral logic remains unchanged
- Degradation remains observable
- Execution intent remains intact

Resilience must never be implicit or hidden.

---

## Consequences of Improper Placement

When resilience is misplaced:

- Business behavior becomes environment-dependent
- Execution paths become implicit
- Failure analysis becomes difficult
- Architecture becomes fragile

Misplaced resilience transforms protection into unpredictability.

---

## Architectural Rule

> Resilience intent is declared by the Application layer  
> and enforced by the Infrastructure layer.

This rule governs all resilience placement decisions.

---

<p align="center">
  <a href="./01-resilience-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-resilience-vs-recovery.md">Next ▶</a>
</p>
