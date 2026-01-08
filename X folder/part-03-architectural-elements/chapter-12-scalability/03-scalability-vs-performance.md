# Scalability vs Performance

## Responsibility

The responsibility of distinguishing scalability from performance is to ensure that **the system’s ability to grow is not confused with the speed at which individual work is executed**.

This boundary preserves architectural clarity by separating *capacity growth* from *execution efficiency*.

---

## Why the Distinction Matters

Scalability and performance are frequently conflated because both influence system responsiveness.

When performance optimizations are treated as scalability strategies, systems become fragile under growth. When scalability concerns are addressed solely through performance tuning, capacity limits are reached silently.

The distinction exists to ensure that:

- Growth does not depend on micro-optimizations
- Execution speed does not redefine system capacity
- Behavior remains consistent under load
- Architectural intent remains clear

---

## Scalability

Scalability defines **capacity growth**.

Scalability:

- Increases the amount of work the system can handle
- Preserves behavior as volume grows
- Enables expansion without redesign
- Is independent of individual execution speed

Scalability answers the question:

> “How does the system handle more of the same work?”

Scalability is an architectural concern.

---

## Performance

Performance defines **execution efficiency**.

Performance:

- Improves how fast individual work completes
- Reduces latency and resource consumption
- Optimizes execution paths
- Is sensitive to implementation details

Performance answers the question:

> “How fast does this work execute?”

Performance is an optimization concern.

---

## The Boundary Between Them

The architectural boundary is strict.

- Scalability increases capacity
- Performance improves speed
- Scalability must not depend on performance gains
- Performance must not redefine correctness or behavior

If the system can only scale by becoming faster, the boundary has been violated.

---

## Growth and Optimization

This distinction preserves sustainable growth.

- Scalability ensures the system can grow safely
- Performance optimizes experience within that capacity
- Growth must not require constant re-optimization
- Optimization must not become a substitute for capacity planning

Architecture must support growth independently of tuning.

---

## Common Boundary Violations

Typical violations include:

- Treating performance tuning as a scalability strategy
- Designing systems that rely on low latency for correctness
- Assuming faster execution equates to higher capacity
- Allowing performance regressions to change behavior

These patterns conflate optimization with architectural capability.

---

## Architectural Rule

> Scalability increases capacity.  
> Performance increases speed.

This separation is non-negotiable.

---

<p align="center">
  <a href="./02-scalability-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-scalability-anti-patterns.md">Next ▶</a>
</p>
