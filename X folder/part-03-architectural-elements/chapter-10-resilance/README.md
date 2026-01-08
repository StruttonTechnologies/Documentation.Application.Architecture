# Resilience

## Overview

Resilience defines the architectural responsibility for **allowing the system to continue operating in the presence of failure, degradation, or partial unavailability without obscuring intent or corrupting behavior**.

Within this architecture, resilience exists to contain failure, limit blast radius, and preserve system stability—without silently altering outcomes or redefining business behavior.

Resilience answers the question:

> “How does the system behave when things go wrong?”

It does not answer:

> “What business outcome should occur?”  
> “Which rules apply?”  
> “How should behavior be coordinated?”

---

## The Role of Resilience in the Architecture

Resilience exists to:

- Contain and isolate failure
- Prevent cascading faults
- Preserve availability where appropriate
- Maintain predictable behavior under stress
- Enable recovery without loss of intent

Resilience protects execution; it does not redefine it.

---

## Architectural Constraints

Resilience is governed by strict architectural constraints to prevent responsibility erosion.

Resilience must:

- Be explicit and intentional
- Preserve original execution intent
- Fail predictably and observably
- Remain orthogonal to business behavior
- Respect architectural boundaries

Resilience must not:

- Encode business rules
- Alter domain outcomes
- Mask failure silently
- Introduce hidden control flow
- Replace explicit recovery design

When resilience changes what the system *does*, the boundary has been violated.

---

## Resilience and Responsibility Boundaries

Resilience operates **around execution**, not within business logic.

Architecturally:

- Behavior defines intent
- Transactions protect consistency
- Error handling reports failure
- Resilience limits impact and enables recovery

Each concern remains distinct. Resilience must not absorb the responsibilities of others.

---

## Resilience and Change

Resilience exists to manage **failure conditions**, not **business evolution**.

Correct resilience design ensures that changes in infrastructure reliability or load do not:

- Alter business logic
- Introduce implicit behavior changes
- Require defensive logic in core layers

Resilience centralizes failure containment while preserving architectural clarity.

---

## Pages in This Section

- **[01 — Resilience Responsibility](./01-resilience-responsibility.md)**  
  Defines resilience as an architectural responsibility and establishes its scope

- **[02 — Resilience Placement](./02-resilience-placement.md)**  
  Explains where resilience belongs in the architecture and where it cannot exist

- **[03 — Resilience vs Recovery](./03-resilience-vs-recovery.md)**  
  Clarifies the boundary between failure tolerance and corrective action

- **[04 — Resilience Anti-Patterns](./04-resilience-anti-patterns.md)**  
  Identifies common architectural violations involving resilience misuse

---

<p align="center">
  <a href="../observability/04-observability-anti-patterns.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-resilience-responsibility.md">Next ▶</a>
</p>
