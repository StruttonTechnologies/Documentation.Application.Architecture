# Explicit Intent

## Responsibility

Dispatcher.Contracts are responsible for **explicitly expressing application intent**.

Each contract represents a specific **Command or Query** the application understands and is willing to process. Contracts define *what is being asked*, not *how it will be done*.

In this architecture, application intent is always expressed as a **Command or a Query**.

Explicit intent ensures that application behavior is discoverable, constrained, and intentional.

---

## Why This Responsibility Exists

Applications degrade when intent is implicit.

When behavior is triggered through loosely defined calls, ad-hoc parameters, or shared models instead of explicit Commands and Queries, the application’s capabilities become unclear. Over time, assumptions replace contracts, and execution paths multiply silently.

Explicit Intent exists to ensure that:

- Application capabilities are clearly defined
- Commands and Queries are intentional and reviewable
- Unsupported behavior cannot be requested accidentally

Contracts turn application behavior into a deliberate API, even internally.

---

## Architectural Implications

When intent is explicit:

- Each Command and Query has a name and purpose
- Execution paths are predictable
- Unsupported actions are impossible to express
- Validation and authorization can be reasoned about consistently

The application becomes **self-describing** at the contract level.

---

## What This Responsibility Protects

Explicit Intent protects:

- **Architectural clarity**  
  What the application does is easy to understand

- **Behavioral discipline**  
  Only supported actions can be requested

- **Change safety**  
  New behavior is introduced intentionally

- **Long-term maintainability**  
  Capabilities do not sprawl invisibly

---

## Consequences of Violation

When intent is implicit or loosely defined:

- Behavior is triggered accidentally
- Similar requests diverge subtly
- Execution logic becomes fragmented
- The application becomes difficult to reason about

Over time, the system shifts from intentional execution to emergent behavior.

---

## Relationship to Other Responsibilities

Explicit Intent reinforces:

- **Contract Stability**  
  Clear intent enables stable contracts

- **Dependency Direction**  
  Intent flows inward through contracts

- **Entry Point Neutrality**  
  All callers speak the same intent language

Together, these responsibilities ensure that Dispatcher.Contracts remain a precise and trustworthy boundary.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-contract-stability.md">Next ▶</a>
</p>
