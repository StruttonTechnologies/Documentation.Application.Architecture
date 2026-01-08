# Error Handling Anti-Patterns

## Responsibility

The responsibility of identifying error handling anti-patterns is to ensure that **failure handling remains explicit, honest, and non-behavioral**.

These anti-patterns describe common failure modes where error handling exceeds its architectural role and obscures intent, authority, or execution flow.

---

## Why Anti-Patterns Matter

Error handling misuse often appears helpful.

What begins as defensive coding or convenience gradually becomes implicit control flow, hidden recovery logic, or surrogate decision-making. Over time, this leads to ambiguous behavior and brittle systems.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Errors as Control Flow

**Anti-pattern:**  
Using errors or exceptions to drive normal execution paths.

When errors determine *what happens next*, failure signaling becomes control flow. This obscures intent and makes behavior difficult to reason about.

Consequences include:

- Implicit branching logic
- Hidden execution paths
- Reduced readability and traceability

Errors must interrupt execution, not direct it.

---

## Errors as Business Outcomes

**Anti-pattern:**  
Using errors to represent expected business results.

Business outcomes are intentional and meaningful. Representing them as errors conflates failure with decision-making.

This leads to:

- Ambiguous semantics
- Loss of domain clarity
- Inconsistent handling

Outcomes must be explicit, not inferred from failure.

---

## Errors as Recovery Mechanisms

**Anti-pattern:**  
Embedding retry, compensation, or recovery logic within error handling.

Error handling exists to report failure, not to resolve it. When recovery is implicit, execution paths become opaque and responsibility becomes unclear.

This introduces:

- Hidden retries
- Unclear failure semantics
- Coupling between failure detection and resolution

Recovery must be explicit and architecturally designed.

---

## Errors as Masking

**Anti-pattern:**  
Catching and suppressing errors to allow execution to continue.

When errors are hidden, systems appear healthy while operating in an invalid state. This undermines trust and observability.

This results in:

- Silent data corruption
- Inconsistent behavior
- Difficult debugging

Errors must be visible.

---

## Errors as Translation

**Anti-pattern:**  
Transforming errors in a way that alters meaning or loses context.

Error translation should preserve intent and context. When meaning is lost, failure analysis becomes difficult and responsibility becomes ambiguous.

This leads to:

- Reduced observability
- Loss of causal information
- Misleading diagnostics

Errors must remain truthful.

---

## Architectural Rule

> If error handling determines behavior,  
> error handling has become control flow.

This rule is absolute.

---

## Architectural Outcome

When error handling anti-patterns are avoided:

- Failure semantics remain clear
- Behavior remains explicit
- Responsibility remains traceable
- Architecture remains trustworthy

Error handling preserves clarity without redefining execution.

---

<p align="center">
  <a href="./03-errors-vs-outcomes.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../observability/README.md">Next ▶</a>
</p>
