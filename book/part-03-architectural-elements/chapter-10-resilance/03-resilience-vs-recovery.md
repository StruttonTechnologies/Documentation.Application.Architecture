# Resilience vs Recovery

## Responsibility

The responsibility of distinguishing resilience from recovery is to ensure that **failure tolerance is not confused with corrective action or system repair**.

This boundary preserves clarity by separating *how the system continues operating under failure* from *how the system is restored to normal operation*.

---

## Why the Distinction Matters

Resilience and recovery are often conflated because both address failure.

When recovery logic is embedded into resilience mechanisms, behavior becomes implicit, execution paths become opaque, and responsibility becomes unclear. The distinction exists to ensure that failure handling remains intentional and observable.

This boundary ensures that:

- Failure tolerance remains predictable
- Corrective action remains explicit
- Execution intent is preserved
- Responsibility remains clearly owned

---

## Resilience

Resilience provides **failure tolerance**.

Resilience:

- Limits blast radius
- Preserves availability where possible
- Allows degraded operation
- Prevents cascading failure

Resilience answers the question:

> “How does the system continue operating when something fails?”

Resilience does not fix the underlying problem.

---

## Recovery

Recovery provides **correction and restoration**.

Recovery:

- Repairs failed components
- Restores normal operation
- Rebuilds lost or inconsistent state
- Resolves underlying causes

Recovery answers the question:

> “How do we return the system to a healthy state?”

Recovery is intentional and explicit.

---

## The Boundary Between Them

The architectural boundary is strict.

- Resilience contains failure
- Recovery resolves failure
- Resilience acts immediately
- Recovery acts deliberately

If resilience mechanisms attempt to repair or correct failure, the boundary has been violated.

---

## Timing and Intent

This distinction preserves intent over time.

- Resilience protects execution *during* failure
- Recovery restores capability *after* failure
- Resilience must not assume recovery success
- Recovery must not be implicit or automatic

Failure tolerance and correction serve different purposes.

---

## Common Boundary Violations

Typical violations include:

- Automatic retries that mask underlying failure
- Silent self-healing without observability
- Recovery logic embedded in resilience mechanisms
- Implicit correction during degraded operation

These patterns replace explicit recovery with hidden behavior.

---

## Architectural Rule

> Resilience tolerates failure.  
> Recovery corrects failure.

This separation is non-negotiable.

---

<p align="center">
  <a href="./02-resilience-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-resilience-anti-patterns.md">Next ▶</a>
</p>
