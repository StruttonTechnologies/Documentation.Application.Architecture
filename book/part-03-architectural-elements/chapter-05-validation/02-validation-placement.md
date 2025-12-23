# Validation Placement

## Responsibility

The responsibility of validation placement is to ensure that **acceptance checks occur at the correct architectural boundary before behavior is executed**.

Proper placement determines whether validation remains a protective gate or becomes an intrusive source of logic. Correct placement preserves clarity, determinism, and responsibility ownership.

---

## Why Placement Matters

Validation is cross-cutting, but it must not be pervasive.

When validation logic is scattered across layers, systems accumulate defensive code, inconsistent failure semantics, and hidden acceptance rules. Placement boundaries exist to ensure that validation is intentional, centralized, and predictable.

Proper placement ensures that:

- Invalid input is rejected early
- Behavioral layers remain focused
- Domain logic assumes correctness
- Failure semantics remain explicit

---

## Placement by Layer

### Presentation Layer

The Presentation layer may perform **surface-level validation**.

This includes checks related to user interaction and transport concerns, such as:

- Structural completeness
- Basic formatting expectations
- Transport constraints

Presentation validation improves user experience but does not define acceptance. Failure here must not be considered authoritative.

---

### Application Layer

The Application layer owns **authoritative validation**.

Responsibilities include:

- Validating command and request intent
- Ensuring required data is present
- Enforcing preconditions for execution
- Rejecting invalid requests before orchestration begins

Validation at this layer is definitive. Behavior does not proceed unless validation succeeds.

---

### Domain Layer

The Domain layer does not perform validation.

Instead, it enforces **invariants**.

Domain logic assumes that input has already been validated and focuses on maintaining truth within the model. Introducing validation here blurs the boundary between acceptance and correctness.

---

### Infrastructure Layer

The Infrastructure layer supports validation but does not define it.

Responsibilities include:

- Technical constraint enforcement
- Integration-level checks
- Supporting validation execution

Infrastructure must not introduce acceptance rules or alter validation outcomes.

---

## Validation at Architectural Boundaries

Validation belongs **between intent and execution**.

Architecturally correct placement ensures that:

- Validation occurs before behavior
- Failure is explicit and traceable
- Execution paths remain clean
- Responsibility remains clear

Validation must never be interleaved with execution.

---

## Consequences of Improper Placement

When validation is misplaced:

- Behavior becomes defensive
- Rules become duplicated
- Failure handling becomes inconsistent
- Architecture becomes opaque

Misplaced validation transforms protection into fragmentation.

---

## Architectural Rule

> Validation occurs before behavior.  
> Behavior assumes validity.

This rule governs all validation placement decisions.

---

<p align="center">
  <a href="./01-validation-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-validation-vs-business-rules.md">Next ▶</a>
</p>
