# Errors vs Outcomes

## Responsibility

The responsibility of distinguishing errors from outcomes is to ensure that **failure signaling is never confused with business results**.

This boundary preserves clarity by separating *what failed during execution* from *what result the business behavior produced*.

---

## Why the Distinction Matters

Errors and outcomes communicate different kinds of information.

When errors are treated as outcomes, or outcomes are inferred from error absence, behavior becomes implicit and ambiguous. The distinction exists to ensure that business intent remains explicit and failure semantics remain truthful.

This boundary ensures that:

- Business results remain intentional
- Failure is not misinterpreted as a decision
- Execution paths remain traceable
- Responsibility remains clear

---

## Errors

Errors represent **execution failure**.

Errors:

- Indicate that execution did not complete as intended
- Preserve context about what failed
- Interrupt normal execution flow
- Require explicit handling or propagation

Errors answer the question:

> “Why could this behavior not complete?”

Errors do not describe business meaning.

---

## Outcomes

Outcomes represent **business results**.

Outcomes:

- Are produced by successful behavior execution
- Express domain-relevant meaning
- May indicate success or domain-level failure
- Are intentional and expected

Outcomes answer the question:

> “What result did this behavior produce?”

Outcomes are authoritative.

---

## The Boundary Between Them

The architectural boundary is strict.

- Errors signal execution failure
- Outcomes signal business meaning
- Errors interrupt execution
- Outcomes complete execution

If business meaning is inferred from error absence, the boundary has been violated.

---

## Failure Is Not an Outcome

Failure of execution is not a business result.

- A failed execution produces no outcome
- An outcome may represent an undesirable business result
- Errors describe inability to produce an outcome
- Outcomes describe the result of completed behavior

This distinction preserves correctness and intent.

---

## Common Boundary Violations

Typical violations include:

- Treating technical errors as business rejection
- Using exceptions to represent business outcomes
- Encoding domain meaning in error types
- Assuming success when no error is raised

These patterns replace explicit outcomes with implicit inference.

---

## Architectural Rule

> Errors describe failure to execute.  
> Outcomes describe business meaning.

This separation is foundational.

---

<p align="center">
  <a href="./02-error-handling-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-error-handling-anti-patterns.md">Next ▶</a>
</p>
