# Dependency Direction

## Responsibility

Dispatcher.Contracts are responsible for enforcing **inward dependency direction** within the application architecture.

All execution logic depends on these contracts, but the contracts themselves depend on nothing beyond shared language constructs. This ensures that intent flows inward, while implementation details remain isolated.

Dependency Direction is enforced structurally, not by convention.

---

## Why This Responsibility Exists

Architectures fail when dependency direction is ambiguous.

If execution logic, orchestration, or infrastructure can influence or reshape application intent, the system becomes fragile. Over time, dependencies reverse unintentionally, abstractions leak, and refactoring becomes risky.

Dependency Direction exists to ensure that:

- Application intent is defined independently of execution
- Implementations cannot shape or redefine contracts
- Architectural boundaries remain enforceable by structure

Clear dependency direction makes architectural violations *impossible*, not merely discouraged.

---

## Architectural Implications

When dependency direction is enforced through Dispatcher.Contracts:

- The Dispatcher depends on contracts, never the reverse
- Orchestration depends on contracts, never the reverse
- Infrastructure is completely unaware of application intent
- Contracts can be reasoned about in isolation

This creates a **stable spine** through the Application layer around which behavior can evolve.

---

## What This Responsibility Protects

Dependency Direction protects:

- **Architectural integrity**  
  Boundaries cannot be crossed accidentally

- **Refactoring safety**  
  Internal changes do not ripple outward

- **Conceptual clarity**  
  Intent remains distinct from execution

- **Long-term scalability**  
  Teams can evolve implementations independently

These protections allow the system to grow without structural decay.

---

## Consequences of Violation

When dependency direction is reversed or blurred:

- Contracts begin reflecting implementation details
- Execution logic leaks outward
- Refactoring requires coordinated change
- Architectural drift accelerates

Over time, the architecture becomes tightly coupled and resistant to change.

---

## Relationship to Other Responsibilities

Dependency Direction reinforces:

- **Explicit Intent**  
  Intent must be defined independently to remain authoritative

- **Contract Stability**  
  Stable contracts depend on correct dependency flow

- **Entry Point Neutrality**  
  All callers depend on the same inward-facing contracts

Together, these responsibilities ensure that Dispatcher.Contracts remain a structurally enforced architectural boundary.

---

<p align="center">
  <a href="./02-contract-stability.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-entry-point-neutrality.md">Next ▶</a>
</p>
