# Cache Invalidation

## Responsibility

The responsibility of cache invalidation is to ensure that **cached data never outlives its correctness**.

Invalidation defines when cached data is no longer valid and must be refreshed or discarded. In this architecture, invalidation is treated as an **architectural concern**, not a low-level implementation detail.

Caching without explicit invalidation rules is not an optimization—it is a risk.

---

## Why Invalidation Is an Architectural Concern

Caching introduces temporal assumptions.

Without explicit invalidation rules, those assumptions become implicit and fragile. Over time, stale data is no longer an edge case—it becomes an expected failure mode that is difficult to reason about or reproduce.

Invalidation must be architecturally defined to ensure that:

- Correctness is preserved under change
- Behavior remains deterministic
- Performance optimizations remain optional
- System behavior can be reasoned about confidently

---

## Invalidation Must Be Explicit

Invalidation must never be accidental.

Architectural invalidation rules must answer:

- What events make cached data invalid?
- Which layer is responsible for invalidation?
- Is invalidation synchronous or eventual?
- What correctness guarantees exist during invalidation windows?

If these questions cannot be answered clearly, caching must not be introduced.

---

## Invalidation Triggers

Common architectural invalidation triggers include:

- Completion of a write operation
- Completion of a workflow
- State transition in a domain entity
- External system updates
- Explicit administrative action

Invalidation triggers must align with **application intent**, not infrastructure convenience.

---

## Layer Responsibilities for Invalidation

### Application Layer

The Application layer owns **intent-driven invalidation**.

When a use case modifies system state, the Application layer is responsible for ensuring that any cached representations affected by that change are invalidated.

This preserves correctness while keeping invalidation tied to explicit behavior.

---

### Infrastructure Layer

The Infrastructure layer may implement **mechanical invalidation**, such as:

- Cache eviction based on keys
- Time-to-live expiration
- Backend-specific invalidation mechanisms

Infrastructure does not decide *when* data becomes invalid—it only enforces invalidation once that decision is made.

---

### Domain Layer

The Domain layer does not manage caching or invalidation.

Domain logic expresses state transitions; it does not track or reason about cached representations of that state.

---

## Time-Based Expiration

Time-based expiration (TTL) may be used **only when correctness allows it**.

TTL must never be used as a substitute for invalidation driven by behavior. When TTL is the sole invalidation mechanism, the system is implicitly accepting periods of incorrect data.

That trade-off must be intentional and explicitly justified.

---

## Architectural Outcome

When cache invalidation is architecturally defined:

- Cached data remains trustworthy
- Behavior remains consistent under load
- Performance optimizations remain safe
- The system resists time-dependent bugs

Invalidation is not a technical nuisance—it is the price of correctness when caching is introduced.

---

<p align="center">
  <a href="./02-caching-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../messaging/README.md">Next ▶</a>
</p>
