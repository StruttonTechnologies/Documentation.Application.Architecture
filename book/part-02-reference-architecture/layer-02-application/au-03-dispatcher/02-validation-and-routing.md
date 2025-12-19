# Validation and Routing

## Responsibility

The Dispatcher is responsible for **validating application intent and routing execution**.

Validation ensures that incoming Commands and Queries are complete and well-formed. Routing determines whether execution proceeds directly to a repository or escalates to orchestration.

---

## Why This Responsibility Exists

Application execution requires decision points.

If validation and routing are scattered, rules are duplicated and execution paths become unpredictable. Over time, simple operations become as complex as workflows, and architectural clarity erodes.

Validation and Routing exist to ensure that:

- Invalid intent is rejected early
- Simple operations remain simple
- Complex workflows are elevated intentionally
- Execution paths are explicit and reviewable

---

## Architectural Implications

When validation and routing are centralized:

- Application-level validation occurs once
- Routing decisions are consistent
- Execution complexity is visible
- Orchestration is used intentionally, not by default

The Dispatcher becomes the **decision point**, not a logic container.

---

## What This Responsibility Protects

Validation and Routing protect:

- **Behavioral consistency**  
  All Commands and Queries follow the same rules

- **Architectural discipline**  
  Complexity is elevated rather than embedded

- **Domain integrity**  
  Only valid intent reaches domain interaction

- **Operational clarity**  
  Execution paths are easy to observe and debug

---

## Consequences of Violation

When validation and routing are not centralized:

- Validation logic is duplicated
- Execution paths diverge
- Handlers accumulate hidden complexity
- Orchestration boundaries blur

Over time, the application becomes fragile and difficult to evolve.

---

## Relationship to Other Responsibilities

Validation and Routing reinforce:

- **Execution Gateway**  
  Routing decisions occur at the gateway

- **Handler Scope and Discipline**  
  Clear routing prevents handlers from becoming workflows

- **Domain Integrity**  
  Invalid intent never reaches the domain

Together, these responsibilities ensure predictable and disciplined execution flow.

---

<p align="center">
  <a href="./01-execution-gateway.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-handler-scope-and-discipline.md">Next ▶</a>
</p>
