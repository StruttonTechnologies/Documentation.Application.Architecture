# Explicit Commit Boundary

## Responsibility

Repository.Contracts define an **explicit commit boundary** through the Unit of Work.

Repositories stage changes.  
The Unit of Work commits them.

This separation makes transactional intent visible and deliberate.

---

## Why This Responsibility Exists

Persistence is not a side effect; it is a decision.

If repositories commit changes implicitly, transactional boundaries become accidental and difficult to reason about. Partial state may be persisted without clear intent.

The explicit commit boundary exists to ensure that:

- Persistence is finalized intentionally
- Workflows define transactional scope
- Partial commits are avoided

---

## Architectural Implications

When the commit boundary is explicit:

- Orchestration controls transactional scope
- Simple handlers remain simple
- Multi-step workflows commit once, at the end
- Failure semantics are predictable

The Application layer defines *when* persistence occurs; Infrastructure defines *how* it happens.

---

## What This Responsibility Protects

The explicit commit boundary protects:

- **Transactional integrity**
- **Workflow correctness**
- **Architectural discipline**

It prevents repositories from becoming hidden transaction managers.

---

## Consequences of Violation

When repositories commit implicitly:

- Transactions fragment
- Partial state persists
- Rollback becomes unclear
- Application behavior becomes unpredictable

Over time, persistence correctness becomes accidental rather than designed.

---

<p align="center">
  <a href="./01-persistence-capabilities.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-dependency-direction.md">Next ▶</a>
</p>
