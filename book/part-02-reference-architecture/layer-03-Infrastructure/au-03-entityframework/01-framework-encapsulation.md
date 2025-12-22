# Framework Encapsulation

## Responsibility

EntityFramework is responsible for **encapsulating the persistence framework**.

Entity Framework types, behaviors, and conventions are confined to this Architectural Unit and are not visible to the Application or Domain layers.

---

## Why This Responsibility Exists

Frameworks evolve, change, and impose constraints.

If framework behavior leaks upward, application logic becomes coupled to technical details and difficult to evolve independently.

Encapsulation ensures that:

- Framework changes do not ripple through the system
- Application logic remains stable
- Persistence technology remains replaceable

---

## Architectural Implications

When frameworks are encapsulated:

- Application logic remains expressive and clean
- Infrastructure complexity is localized
- Replacement or upgrade paths remain viable

Entity Framework becomes a **tool**, not a design driver.

---

## What This Responsibility Protects

Framework Encapsulation protects:

- **Layer isolation**
- **Long-term maintainability**
- **Architectural freedom**

---

## Consequences of Violation

When framework details leak:

- Application logic becomes infrastructure-aware
- Refactoring becomes risky
- Architectural boundaries weaken

Over time, the framework begins to dictate design.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-persistence-execution.md">Next ▶</a>
</p>
