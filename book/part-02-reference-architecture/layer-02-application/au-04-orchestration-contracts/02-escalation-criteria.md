# Escalation Criteria

## Responsibility

Orchestration.Contracts define **when execution escalates from simple handling to coordinated workflows**.

Not all Commands require orchestration. Escalation occurs only when behavior involves multiple steps, cross-entity interaction, or conditional coordination.

---

## Why This Responsibility Exists

Without clear escalation criteria, orchestration becomes either:

- Overused, introducing unnecessary complexity, or
- Avoided, forcing workflows into handlers

Escalation Criteria exist to ensure that:

- Simple execution remains simple
- Complex behavior is elevated intentionally
- Architectural boundaries remain meaningful

---

## Architectural Implications

Clear escalation criteria ensure that:

- Handlers make routing decisions, not coordination decisions
- Orchestration remains purposeful
- Workflow boundaries are respected

This keeps the Application layer balanced rather than polarized.

---

## Relationship to Other Responsibilities

Escalation Criteria reinforce:

- **Validation and Routing**  
  Routing decisions include escalation

- **Workflow Intent**  
  Only defined workflows are executed

---

<p align="center">
  <a href="./01-workflow-intent.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-contract-stability.md">Next ▶</a>
</p>
