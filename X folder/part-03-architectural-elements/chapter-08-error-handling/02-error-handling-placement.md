# Error Handling Placement

## Responsibility

The responsibility of error handling placement is to ensure that **failure is detected and propagated at the correct architectural boundary without leaking control logic into execution paths**.

Correct placement preserves clarity of intent, keeps failure semantics explicit, and prevents error handling from becoming implicit orchestration.

---

## Why Placement Matters

Error handling is inherently cross-cutting, but it must not be pervasive.

When error handling logic is scattered across layers, failure semantics become inconsistent, execution becomes defensive, and responsibility becomes unclear. Placement boundaries exist to ensure that error handling remains intentional, centralized, and predictable.

Proper placement ensures that:

- Failures are surfaced where they occur
- Failure propagation is consistent
- Behavioral logic remains focused
- Recovery remains explicit

---

## Placement by Layer

### Presentation Layer

The Presentation layer handles **representation of failure**, not detection.

Responsibilities include:

- Translating failure into user-facing feedback
- Preserving failure context without reinterpretation
- Avoiding suppression or transformation of failure semantics

Presentation does not decide recovery or retry behavior.

---

### Application Layer

The Application layer owns **failure propagation and categorization**.

Responsibilities include:

- Propagating failures across architectural boundaries
- Maintaining execution intent under failure
- Distinguishing expected failure from unexpected error
- Preventing silent continuation

The Application layer does not recover implicitly.

---

### Domain Layer

The Domain layer signals **rule violation or invariant breach**, not error handling.

Domain logic expresses failure as part of business behavior. It does not catch, translate, or suppress errors.

Domain failures are explicit and intentional.

---

### Infrastructure Layer

The Infrastructure layer detects **technical failures**.

Responsibilities include:

- Detecting infrastructure faults
- Reporting failure accurately
- Preserving low-level failure context

Infrastructure does not decide recovery or behavioral outcomes.

---

## Error Handling at Architectural Boundaries

Error handling belongs **along execution paths**, not inside them.

Architecturally correct placement ensures that:

- Failures are detected at their source
- Propagation remains explicit
- Behavior does not absorb or reinterpret failure
- Responsibility remains traceable

Error handling must never replace explicit recovery design.

---

## Consequences of Improper Placement

When error handling is misplaced:

- Failures are hidden or misclassified
- Behavior becomes defensive and unclear
- Recovery becomes implicit
- Architecture loses transparency

Misplaced error handling transforms clarity into confusion.

---

## Architectural Rule

> Failures are detected where they occur  
> and propagated without reinterpretation.

This rule governs all error handling placement decisions.

---

<p align="center">
  <a href="./01-error-handling-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-errors-vs-outcomes.md">Next ▶</a>
</p>
