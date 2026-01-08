# Execution Delegation

## Responsibility

Frontend Architectural Units are responsible for **expressing intent**, not executing application behavior.

Frontends initiate requests and present results, but all execution occurs elsewhere.

---

## Why This Responsibility Exists

Frontends are optimized for interaction, not coordination.

If execution logic is allowed to exist in the frontend, behavior becomes fragmented and inconsistent. Different clients begin to enforce different rules, and the system loses coherence.

Execution Delegation exists to ensure that:

- Application behavior remains centralized
- Workflows are consistent across clients
- Rules are enforced uniformly

---

## Architectural Implications

When execution is delegated:

- Frontends remain thin and replaceable
- Application behavior has a single source of truth
- Testing and validation are centralized

Frontends become consumers of behavior, not owners of it.

---

## What This Responsibility Protects

Execution Delegation protects:

- **Behavioral cohesion**
- **Architectural clarity**
- **Consistency across clients**

---

## Consequences of Violation

If frontends begin executing behavior:

- Business rules diverge
- Bugs appear only in certain clients
- System behavior becomes unpredictable

Over time, the application ceases to function as a unified whole.

---

## Relationship to Other Responsibilities

Execution Delegation works in concert with:

- **Client Independence**
- **Boundary Enforcement**
- **Contract Stability**

Together, these responsibilities ensure that behavior remains centralized and authoritative.

---

<p align="center">
  <a href="./01-client-independence.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-boundary-enforcement.md">Next ▶</a>
</p>
