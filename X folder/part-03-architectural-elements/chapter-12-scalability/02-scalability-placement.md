# Scalability Placement

## Responsibility

The responsibility of scalability placement is to ensure that **capacity growth mechanisms are applied at the correct architectural boundaries without leaking scalability concerns into business behavior or domain logic**.

Correct placement preserves behavioral consistency, prevents load-driven semantics, and keeps growth concerns isolated from intent.

---

## Why Placement Matters

Scalability pressures often surface gradually.

When scalability mechanisms are embedded directly into behavior, growth changes meaning. Load conditions begin to influence outcomes, and architecture drifts from intentional design to reactive optimization.

Placement rules exist to ensure that scalability remains a capacity concern rather than a behavioral one.

Proper placement ensures that:

- Growth does not alter outcomes
- Behavior remains load-independent
- Capacity decisions remain explicit
- Responsibility boundaries remain intact

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not manage scalability.

Presentation concerns may reflect degraded responsiveness or capacity limits, but they must not alter behavior based on load. Introducing scalability logic here couples user interaction to system capacity.

Presentation communicates limits; it does not manage growth.

---

### Application Layer

The Application layer defines **scalability intent**.

Responsibilities include:

- Declaring which interactions must scale
- Defining acceptable capacity growth boundaries
- Preserving behavior semantics under increased load

The Application layer decides *where* scalability applies, not *how* it is achieved.

---

### Domain Layer

The Domain layer is unaware of scalability concerns.

Domain logic expresses business truth and correctness. Introducing scalability logic here couples domain meaning to volume and violates architectural independence.

Domain behavior must remain identical regardless of load.

---

### Infrastructure Layer

The Infrastructure layer implements **scalability mechanisms**.

Responsibilities include:

- Allocating and managing capacity
- Distributing workload safely
- Handling resource contention
- Supporting horizontal or vertical growth

Infrastructure enforces scalability; it does not define intent.

---

## Scalability at Architectural Boundaries

Scalability belongs **around execution boundaries**, not within domain behavior.

Architecturally correct placement ensures that:

- Capacity can grow transparently
- Behavior remains unchanged
- Load handling remains observable
- Responsibility remains clear

Scalability must never be implicit or hidden.

---

## Consequences of Improper Placement

When scalability is misplaced:

- Business behavior becomes volume-dependent
- Execution semantics vary under load
- Testing becomes environment-specific
- Architecture becomes brittle under growth

Misplaced scalability transforms growth into risk.

---

## Architectural Rule

> Scalability intent is declared by the Application layer  
> and enforced by the Infrastructure layer.

This rule governs all scalability placement decisions.

---

<p align="center">
  <a href="./01-scalability-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-scalability-vs-performance.md">Next ▶</a>
</p>
