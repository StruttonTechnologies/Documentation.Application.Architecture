# Configuration vs Behavior

## Responsibility

The responsibility of distinguishing configuration from behavior is to ensure that **declarative context never becomes executable logic**.

This boundary preserves architectural clarity by keeping environmental concerns separate from decision-making and execution.

---

## Why the Distinction Matters

Configuration and behavior address fundamentally different concerns.

When configuration is allowed to influence behavior, execution paths become implicit, outcomes become environment-dependent, and the architecture loses determinism. The distinction exists to ensure that behavior remains intentional and explicit.

This boundary ensures that:

- Decisions are traceable to application intent
- Logic remains testable and predictable
- Environment does not become a hidden control mechanism

---

## Configuration

Configuration describes **context**.

Configuration is:

- Declarative
- External to execution
- Evaluated at composition time
- Stable across execution paths
- Independent of runtime input

Configuration answers the question:

> “What environment is this system operating within?”

Configuration does not execute logic and does not react to conditions.

---

## Behavior

Behavior describes **action**.

Behavior is:

- Executable
- Contextual and input-driven
- Evaluated at runtime
- Capable of success or failure
- Governed by rules and constraints

Behavior answers the question:

> “What should the system do now?”

Behavior is always explicit and intentional.

---

## The Boundary Between Them

The architectural boundary is strict.

- Configuration may shape how behavior is assembled
- Behavior may not be altered by configuration at runtime
- Configuration supplies values; behavior interprets inputs
- Configuration informs structure; behavior produces outcomes

If configuration must be read to understand execution paths, the boundary has been violated.

---

## Determinism and Traceability

This distinction preserves determinism.

Given the same configuration and the same inputs:

- Behavior must execute identically
- Outcomes must be explainable
- Execution paths must remain observable

Configuration-driven behavior introduces hidden branching and undermines traceability.

---

## Common Boundary Violations

Typical violations include:

- Configuration flags that alter business rules
- Environment-driven conditional logic
- Feature toggles that bypass validation
- Configuration-based workflow selection
- Context-dependent rule enforcement

These patterns replace explicit design with implicit control.

---

## Architectural Rule

> Configuration describes context.  
> Behavior performs action.  
> Context must never decide action.

This rule governs all interactions between configuration and behavior.

---

<p align="center">
  <a href="./02-configuration-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-configuration-anti-patterns.md">Next ▶</a>
</p>
