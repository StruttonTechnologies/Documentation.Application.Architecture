# Layer Registrars

## Responsibility

Each architectural layer exposes a **registrar** responsible for registering that layer’s services into an `IServiceCollection`.

Registrars define *what the layer contributes* without knowing *how the application is assembled*.

---

## Why This Responsibility Exists

Allowing layers to self-register services avoids central knowledge of internal details.

If a single location were responsible for registering every service directly, it would need intimate knowledge of each layer’s internal structure.

Layer registrars ensure that:
- Each layer owns its own registrations
- Internal structure remains encapsulated
- Registration logic remains localized

---

## Architectural Implications

When layers expose registrars:

- Composition becomes declarative
- Layers remain independently evolvable
- Infrastructure details do not leak upward

Registrars express **capabilities**, not implementations.

---

## What This Responsibility Protects

Layer Registrars protect:

- **Encapsulation**
- **Layer autonomy**
- **Architectural clarity**

---

## Consequences of Violation

When registration logic is centralized without registrars:

- Internal details leak
- Startup code becomes brittle
- Changes cascade across layers

Over time, composition becomes tightly coupled and difficult to evolve.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-centralized-composition.md">Next ▶</a>
</p>
