# Caching Placement

## Responsibility

The responsibility of caching placement is to ensure that **performance optimizations respect architectural boundaries**.

Caching may exist in multiple layers, but only where it does not compromise determinism, dependency direction, or separation of concerns. Placement determines whether caching remains an optimization or becomes a hidden behavioral dependency.

---

## Why Placement Matters

Caching is not neutral.

Where caching is introduced determines:
- Which layer owns correctness
- Which layer controls invalidation
- How change propagates through the system

Poor placement allows performance concerns to leak into business logic, making behavior dependent on timing and cache state rather than intent.

Explicit placement rules exist to preserve architectural reasoning.

---

## Placement by Layer

### Presentation Layer

Caching in the Presentation layer is limited to **presentation artifacts**.

Appropriate caching includes:
- Rendered responses
- Static or semi-static view models
- Client-facing representations

Presentation caching must not:
- Cache application behavior
- Bypass application contracts
- Encode business decisions

Presentation caching optimizes delivery, not execution.

---

### Application Layer

Caching in the Application layer may be used to optimize **use-case results**.

Appropriate caching includes:
- Idempotent query results
- Read-only use-case outcomes
- Derived data with explicit invalidation rules

Application-layer caching must:
- Be explicit and intentional
- Preserve correctness under invalidation
- Remain transparent to callers

Application caching must not:
- Cache domain state
- Replace orchestration logic
- Obscure transactional boundaries

---

### Domain Layer

The Domain layer does not cache.

Domain logic must remain:
- Deterministic
- State-driven
- Independent of infrastructure concerns

Caching within the Domain would introduce temporal state and violate the expectation that domain behavior is fully determined by input and state.

---

### Infrastructure Layer

Caching in the Infrastructure layer is a **technical optimization**.

Appropriate caching includes:
- Data access results
- External system responses
- Resource-intensive integration calls

Infrastructure caching must:
- Respect data consistency guarantees
- Remain invisible to higher layers
- Avoid leaking implementation details

Infrastructure caching improves efficiency, not semantics.

---

## Cross-Layer Cache Interaction

Caching must never span layers in a way that exposes implementation detail.

- Higher layers may benefit from caching
- Lower layers may implement caching
- No layer may assume another layer’s cache behavior

Caching behavior must remain local to the layer that owns it.

---

## Architectural Outcome

When caching placement is respected:

- Performance improves without altering behavior
- Layers remain independently reasoned about
- Invalidation rules remain explicit
- Caching remains optional and safe

Caching becomes a controlled optimization rather than an architectural liability.

---

<p align="center">
  <a href="./01-caching-boundaries.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-cache-invalidation.md">Next ▶</a>
</p>
