# Enforcing Dependency Direction

Defining dependency direction is only effective if it is consistently enforced.
Architectural rules that rely on discipline or convention eventually erode as systems
grow and teams change.

This subsection explains how dependency direction is enforced structurally and why
enforcement must be built into the architecture itself.

---

## Enforcement Through Structure

In this architecture, dependency direction is enforced through structural constraints
rather than policy.

These constraints include:

- Explicit project references
- Contract-based boundaries
- Clear separation between abstraction and implementation
- Centralized composition

By encoding dependency rules into the structure of the system, violations become
impossible rather than discouraged.

---

## Contracts as Dependency Anchors

Contracts serve as the stable anchors around which dependencies are organized.

Both high-level policy and low-level implementation depend on the same contract, but
neither depends on the other directly. This shared dependency point enforces inversion
and preserves independence.

Contracts are intentionally placed at boundary edges rather than embedded within
implementations.

---

## Preventing Backward Dependencies

Backward dependencies—where higher-level components depend on lower-level details—are
one of the most common sources of architectural decay.

Structural enforcement prevents these dependencies by:

- Restricting project visibility
- Limiting reference paths
- Ensuring implementations are not accessible outside their boundary

If a dependency cannot be expressed structurally, it cannot exist in the system.

---

## Centralized Composition

Composition is the single point where dependency direction is intentionally crossed.

Rather than allowing components to compose themselves, this architecture centralizes
composition in a designated location. This ensures that dependency inversion is explicit,
reviewable, and consistent.

Centralized composition completes the enforcement model by allowing controlled wiring
without violating architectural rules.

---

## Enforcement Enables Trust

When dependency direction is enforced structurally, teams no longer need to rely on
constant vigilance during code reviews.

Architectural correctness becomes a property of the system rather than a matter of
individual discipline. This enables trust, scalability, and long-term maintainability.

---

## Transition to the Reference Architecture

With boundaries, visibility, and dependency direction established, the architecture is
now ready to define concrete layers and responsibilities.

The next part of this book introduces the reference architecture and explains how these
foundational principles are applied in practice.

---

## Composition as Boundary Enforcement

Architectural boundaries are not enforced solely through contracts and dependency direction.

They are also enforced through **centralized composition**, where concrete implementations are wired explicitly at the application boundary.

By confining composition to a single, well-defined location, the architecture ensures that:
- Layers remain isolated
- Dependencies remain directional
- Implementations remain swappable

Composition is therefore not an incidental startup concern, but an intentional enforcement mechanism that supports all other architectural rules.

---

<p align="center">
  <a href="./subsection-02-dependency-vs-call-direction.md">◀ Previous Subsection</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../../part-02-reference-architecture/README.md">Next Part ▶</a>
</p>
