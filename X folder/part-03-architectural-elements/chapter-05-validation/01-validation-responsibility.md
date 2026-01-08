# Validation Responsibility

## Responsibility

The responsibility of validation in this architecture is to **determine whether input, intent, or state satisfies required constraints before behavior is executed**.

Validation acts as a gate. It protects the system from invalid input without performing orchestration, enforcing policy, or executing business logic.

---

## Why This Responsibility Exists

Behavior assumes correctness.

Without explicit validation boundaries, behavioral layers must defensively handle malformed input, missing data, and structural inconsistencies. This scatters acceptance logic across the system and obscures intent.

Validation exists to ensure that:

- Invalid input is rejected early
- Failure is explicit and predictable
- Behavioral logic remains focused and intentional
- Responsibility remains centralized and observable

---

## What Validation Is Allowed to Do

Validation may:

- Evaluate structural correctness
- Verify presence and format of required data
- Enforce preconditions for execution
- Reject input that cannot be processed safely
- Provide clear reasons for rejection

Validation may prevent execution, but it must not determine outcomes.

---

## What Validation Must Never Do

Validation must not:

- Execute behavior
- Perform orchestration
- Encode business policy
- Decide success or failure semantics
- Trigger side effects
- Modify state

If validation determines *what should happen next*, it has exceeded its responsibility.

---

## Validation as Acceptance, Not Judgment

Validation determines **acceptability**, not **desirability**.

- Acceptance asks: “Is this input valid?”
- Judgment asks: “Is this action allowed or correct?”

Judgment belongs to policy and domain logic. Validation only answers whether processing may proceed.

---

## Determinism and Transparency

Validation must be deterministic and transparent.

Given the same input and the same context:

- Validation results must be consistent
- Failures must be explainable
- Acceptance criteria must be observable

Validation that depends on hidden state or environmental factors violates architectural intent.

---

## Consequences of Boundary Violation

When validation exceeds its responsibility:

- Business rules become implicit
- Decision-making becomes fragmented
- Failure semantics become unclear
- Architecture becomes difficult to reason about

Validation shifts from protection to control.

---

## Architectural Rule

> Validation determines acceptability.  
> Behavior determines outcome.

This separation is foundational.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-validation-placement.md">Next ▶</a>
</p>
