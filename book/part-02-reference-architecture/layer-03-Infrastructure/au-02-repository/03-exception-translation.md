# Exception Translation

## Responsibility

Repositories are responsible for **translating technical persistence exceptions** into application-safe errors.

They do not expose raw framework exceptions to the Application layer.

---

## Why This Responsibility Exists

Persistence technologies fail in implementation-specific ways.

If framework exceptions leak upward, the Application layer becomes coupled to storage details and error handling becomes inconsistent.

Exception translation ensures that:

- Application code handles predictable error types
- Infrastructure details remain encapsulated
- Failure semantics are consistent

---

## Architectural Implications

When repositories translate exceptions:

- Error handling is centralized
- Application logic remains storage-agnostic
- Infrastructure failures do not shape behavior

Repositories act as a **protective boundary**, not a source of behavior.

---

## What This Responsibility Protects

Exception Translation protects:

- **Layer isolation**
- **Error consistency**
- **Future replaceability**

---

## Consequences of Violation

When framework exceptions leak:

- Application logic becomes infrastructure-aware
- Error handling fragments
- Architectural boundaries weaken

Over time, failure handling becomes unpredictable and tightly coupled.

---

<p align="center">
  <a href="./02-no-commit-no-coordination.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-03-entityframework/README.md">Next ▶</a>
</p>
