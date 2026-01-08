# Centralized Composition

## Responsibility

Application composition is **centralized** into a single location that aggregates registrations from all layers.

This location is responsible for assembling the complete application object graph.

---

## Why This Responsibility Exists

Composition requires knowledge of **all participating layers**.

Centralizing composition ensures that:
- Dependencies are visible and intentional
- Wiring decisions are explicit
- The application startup path is predictable

Decentralized composition fragments responsibility and obscures dependency relationships.

---

## Architectural Implications

When composition is centralized:

- Dependency direction is enforced structurally
- Application startup remains transparent
- Infrastructure remains replaceable

Centralized composition acts as a **final architectural checkpoint**.

---

## What This Responsibility Protects

Centralized Composition protects:

- **Dependency integrity**
- **Startup predictability**
- **Architectural enforceability**

---

## Consequences of Violation

When composition is scattered:

- Dependencies become implicit
- Startup behavior becomes opaque
- Boundaries erode silently

Over time, the architecture becomes difficult to reason about or modify safely.

---

<p align="center">
  <a href="./01-layer-registrars.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-program-entry-point.md">Next ▶</a>
</p>
