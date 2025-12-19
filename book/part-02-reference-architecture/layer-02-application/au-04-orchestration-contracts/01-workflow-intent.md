# Workflow Intent

## Responsibility

Orchestration.Contracts are responsible for **explicitly expressing workflow intent**.

A workflow represents coordinated behavior involving multiple steps, decisions, or state transitions. These workflows are expressed as first-class contracts rather than implicit sequences embedded in handlers.

---

## Why This Responsibility Exists

Not all behavior is simple execution.

When coordination logic is embedded directly in handlers, complexity becomes hidden and duplicated. Over time, handlers become workflows in disguise.

Workflow Intent exists to ensure that:

- Coordinated behavior is named and intentional
- Workflows are visible and reviewable
- Complexity is elevated rather than buried

Explicit workflows make complexity explicit.

---

## Architectural Implications

When workflow intent is explicit:

- Handlers remain focused and disciplined
- Coordination logic has a single home
- Execution paths are easier to reason about
- Testing and evolution become safer

Workflows become **application capabilities**, not implementation accidents.

---

## Relationship to Other Responsibilities

Workflow Intent reinforces:

- **Handler Scope and Discipline**  
  Handlers do not become workflow engines

- **Escalation Criteria**  
  Only appropriate behavior is elevated

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-escalation-criteria.md">Next ▶</a>
</p>
