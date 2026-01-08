# Section — Dependency Direction

Dependency direction defines *who is allowed to depend on whom* within the system.

In the Core Application Architecture, dependency direction is a strict architectural rule,
not an emergent property of code organization. It determines how responsibilities are
isolated, how change propagates, and how the system remains stable over time.

This section explains why dependency direction matters, how it is enforced, and how it
shapes the overall structure of the architecture.

---

## Purpose of This Section

The purpose of this section is to establish a clear and enforceable model for dependency
direction across the system.

Specifically, this section answers:

- Why unrestricted dependencies lead to architectural decay
- How dependency direction preserves boundaries
- How contracts and dependency direction work together
- Why composition must be centralized

These concepts are foundational for understanding the layered model introduced later in
this book.

---

## Dependency Direction Is Not Call Direction

A common source of confusion is the assumption that dependency direction follows call
direction. In practice, these two concepts are independent.

A component may call into another component without depending on its implementation.
Dependency direction is determined by *who knows about whom*, not who invokes whom at
runtime.

This distinction is critical to maintaining architectural integrity.

---

## Dependencies Define Knowledge

When one part of the system depends on another, it gains knowledge of that part’s types,
contracts, and responsibilities.

Over time, unrestricted knowledge leads to:

- Tight coupling
- Reduced ability to change components independently
- Implicit architectural assumptions

Controlling dependency direction limits knowledge flow and preserves intentional design.

---

## Dependency Direction as an Architectural Constraint

In this architecture, dependency direction is treated as a constraint that must be
satisfied at all times.

Projects are structured so that:

- Higher-level policy does not depend on lower-level detail
- Implementation details depend on stable abstractions
- Contracts sit at boundary points, not within implementations

These constraints are enforced structurally rather than through convention.

---

## Preparing for the Layered Model

Dependency direction provides the foundation for the layered architecture described in
the next part of this book.

Once dependency direction is established, layers can be defined with clear
responsibilities, predictable interaction patterns, and enforceable boundaries.

---

<p align="center">
  <a href="../section-boundaries-and-visibility/README.md">◀ Previous Section</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <span style="opacity: 0.5;">Subsections coming next ▶</span>
</p>
