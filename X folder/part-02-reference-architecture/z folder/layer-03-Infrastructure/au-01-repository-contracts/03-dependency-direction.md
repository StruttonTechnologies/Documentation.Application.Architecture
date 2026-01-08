# Dependency Direction

## Responsibility

Repository.Contracts enforce **correct dependency direction** between the Application and Infrastructure layers.

The Application depends on repository contracts.  
Infrastructure implements them.

The reverse is not permitted.

---

## Why This Responsibility Exists

If Infrastructure depends on Application behavior, boundaries collapse.

Clear dependency direction ensures that application behavior remains stable while infrastructure details evolve independently.

---

## Architectural Implications

When dependency direction is enforced:

- Application logic is isolated from storage details
- Infrastructure changes do not ripple upward
- Architectural layers remain distinct and enforceable

Dependency direction is structural, not advisory.

---

## What This Responsibility Protects

Dependency Direction protects:

- **Layer isolation**
- **Long-term maintainability**
- **Architectural enforceability**

---

## Consequences of Violation

When dependency direction is violated:

- Infrastructure shapes application behavior
- Refactoring becomes risky
- Layer boundaries lose meaning

Over time, the architecture devolves into a coupled system.

---

<p align="center">
  <a href="./02-explicit-commit-boundary.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-02-repository/README.md">Next ▶</a>
</p>
