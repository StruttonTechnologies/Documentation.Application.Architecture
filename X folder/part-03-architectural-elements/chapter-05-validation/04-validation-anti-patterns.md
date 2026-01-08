# Validation Anti-Patterns

## Responsibility

The responsibility of identifying validation anti-patterns is to ensure that **validation remains a protective acceptance gate and does not evolve into decision-making, policy enforcement, or behavior execution**.

These anti-patterns describe common failure modes where validation exceeds its architectural role and erodes responsibility boundaries.

---

## Why Anti-Patterns Matter

Validation misuse often appears benign.

What begins as a convenience gradually becomes implicit policy, hidden decision logic, or duplicated domain rules. Over time, this results in unclear authority, inconsistent outcomes, and fragile behavior.

Anti-patterns exist to make these failures explicit and prevent architectural drift.

---

## Validation as Business Logic

**Anti-pattern:**  
Embedding business rules within validation checks.

When validation determines whether an action is *allowed* rather than whether input is *acceptable*, it assumes domain authority.

Consequences include:

- Business rules becoming implicit
- Domain logic losing central ownership
- Acceptance failures masking true decision outcomes

Validation must never evaluate correctness.

---

## Validation as Orchestration

**Anti-pattern:**  
Triggering workflows, side effects, or coordination during validation.

Validation is not an execution phase. When it performs orchestration, execution paths become fragmented and responsibility becomes unclear.

This leads to:

- Side effects occurring before acceptance
- Inconsistent execution semantics
- Hidden coupling between validation and behavior

Validation must remain side-effect free.

---

## Validation as Policy Enforcement

**Anti-pattern:**  
Using validation to enforce authorization, entitlements, or policy decisions.

Policy enforcement requires context, authority, and intent. Validation provides none of these.

When validation enforces policy:

- Decisions lack traceability
- Authority becomes ambiguous
- Policy changes bypass architectural review

Policy belongs to dedicated decision-making mechanisms.

---

## Validation as Error Handling

**Anti-pattern:**  
Using validation to compensate for failures in downstream behavior.

Validation exists to prevent invalid input, not to manage execution failures. When validation is used to mask or anticipate behavior errors, failure semantics become distorted.

This results in:

- Misleading error signals
- Defensive duplication
- Reduced observability

Failures must be handled where they occur.

---

## Validation as Runtime State

**Anti-pattern:**  
Making validation dependent on mutable or hidden runtime state.

Validation must be deterministic and repeatable. When acceptance depends on transient conditions or hidden state, results become unpredictable.

This introduces:

- Inconsistent acceptance outcomes
- Temporal coupling
- Difficult-to-reproduce defects

Validation must rely only on explicit input and stable context.

---

## Architectural Rule

> If validation determines outcomes,  
> validation has become behavior.

This rule is absolute.

---

## Architectural Outcome

When validation anti-patterns are avoided:

- Acceptance remains explicit
- Authority remains clear
- Behavior remains intentional
- Architecture remains legible

Validation protects the system without controlling it.

---

<p align="center">
  <a href="./03-validation-vs-business-rules.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../security/README.md">Next ▶</a>
</p>
