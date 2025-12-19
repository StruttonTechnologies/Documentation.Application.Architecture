# No Commit, No Coordination

## Responsibility

Repositories **do not commit persistence** and **do not coordinate execution**.

They stage changes only. The decision to finalize persistence is made explicitly by the Application layer through the Unit of Work.

---

## Why This Responsibility Exists

Persistence is a decision, not a side effect.

If repositories commit changes implicitly, transactional boundaries become unclear and workflows lose control over correctness.

Separating staging from committing ensures that:

- Transactions are intentional
- Workflows define persistence scope
- Partial commits are avoided

---

## Architectural Implications

When repositories do not commit or coordinate:

- Simple handlers remain simple
- Workflows commit once, at the end
- Persistence boundaries are visible and predictable

Repositories remain subordinate to orchestration rather than controlling it.

---

## What This Responsibility Protects

No Commit, No Coordination protects:

- **Transactional integrity**
- **Workflow correctness**
- **Architectural discipline**

---

## Consequences of Violation

When repositories commit or coordinate:

- Transactions fragment
- Persistence becomes unpredictable
- Workflow intent is undermined

Over time, repositories become hidden controllers rather than infrastructure mechanisms.

---

<p align="center">
  <a href="./01-data-access-only.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-exception-translation.md">Next ▶</a>
</p>
