# Security

## Overview

Security defines the architectural responsibility for **protecting the system from unauthorized access, misuse, and unintended exposure while preserving explicit intent and responsibility boundaries**.

Within this architecture, security exists to constrain *who may act*, *what may be accessed*, and *how interactions are protected*—without obscuring behavior or embedding policy into inappropriate layers.

Security answers the question:

> “Who is allowed to do this, and under what constraints?”

It does not answer:

> “What should the system do next?”  
> “How should work be coordinated?”  
> “What business outcome should occur?”

---

## The Role of Security in the Architecture

Security exists to:

- Protect system boundaries
- Establish trust and identity
- Enforce access constraints
- Prevent unauthorized interaction
- Preserve system integrity under hostile conditions

Security constrains behavior; it does not define it.

---

## Architectural Constraints

Security is governed by strict architectural constraints to prevent responsibility erosion.

Security must:

- Be explicit and observable
- Enforce access at defined boundaries
- Remain orthogonal to business behavior
- Fail closed and predictably
- Preserve intent clarity

Security must not:

- Encode business rules
- Perform orchestration
- Determine business outcomes
- Replace validation or domain logic
- Obscure execution paths

When security logic alters behavior semantics, the boundary has been violated.

---

## Security and Responsibility Boundaries

Security operates at **architectural entry points**.

Architecturally:

- Security evaluates *who* is acting
- Validation evaluates *whether input is acceptable*
- Domain logic evaluates *what is correct*
- Behavior executes only after all constraints are satisfied

Security constrains execution; it does not coordinate it.

---

## Security and Change

Security exists to manage **access change**, not **behavior change**.

Correct security design ensures that changes in identity, credentials, or threat posture do not:

- Alter business logic
- Introduce hidden execution paths
- Require defensive behavior across layers

Security centralizes access control and makes enforcement explicit.

---

## Pages in This Section

- **[01 — Security Responsibility](./01-security-responsibility.md)**  
  Defines security as an architectural responsibility and establishes its authority boundaries

- **[02 — Security Placement](./02-security-placement.md)**  
  Explains where security belongs in the architecture and where it cannot exist

- **[03 — Security vs Business Logic](./03-security-vs-business-logic.md)**  
  Clarifies the boundary between access control and domain behavior

- **[04 — Security Anti-Patterns](./04-security-anti-patterns.md)**  
  Identifies common architectural violations involving security misuse

---

<p align="center">
  <a href="../validation/04-validation-anti-patterns.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-security-responsibility.md">Next ▶</a>
</p>
