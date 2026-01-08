# Program Entry Point

## Responsibility

The application entry point is responsible for **invoking composition**, not performing it.

It initializes the application by:
- Creating the service collection
- Delegating registration to the composition mechanism
- Building and running the application

---

## Why This Responsibility Exists

The entry point should remain minimal.

If startup logic accumulates here, it becomes difficult to test, reason about, and evolve.

Delegating composition ensures that:
- Startup remains thin
- Composition logic remains reusable
- Application configuration remains explicit

---

## Architectural Implications

When the entry point is thin:

- Startup behavior is predictable
- Environment-specific configuration is isolated
- Architectural intent remains visible

The entry point coordinates startup; it does not define architecture.

---

## What This Responsibility Protects

The Program Entry Point protects:

- **Startup clarity**
- **Separation of concerns**
- **Long-term maintainability**

---

## Consequences of Violation

When the entry point becomes complex:

- Configuration logic sprawls
- Startup behavior becomes fragile
- Architectural intent is obscured

Over time, the application becomes difficult to initialize correctly.

---

<p align="center">
  <a href="./02-centralized-composition.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../README.md">Next ▶</a>
</p>
