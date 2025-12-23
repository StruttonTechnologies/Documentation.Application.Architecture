# Security Placement

## Responsibility

The responsibility of security placement is to ensure that **access constraints are enforced at architectural entry points without leaking authorization logic into behavioral execution paths**.

Correct placement preserves clarity of intent, centralizes authority, and prevents security from becoming implicit or fragmented.

---

## Why Placement Matters

Security is inherently cross-cutting, but it must not be pervasive.

When security checks are scattered across layers, authorization becomes inconsistent, behavior becomes conditional, and responsibility becomes unclear. Placement boundaries exist to ensure that access control is explicit, centralized, and predictable.

Proper placement ensures that:

- Unauthorized requests are rejected early
- Behavioral layers remain focused on execution
- Authorization decisions are traceable
- Architectural boundaries remain intact

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not own security decisions.

Presentation concerns may participate in identity capture or credential transport, but they must not authorize access or enforce policy. Allowing security decisions here introduces duplication and bypass risk.

Presentation expresses intent; it does not grant permission.

---

### Application Layer

The Application layer owns **authoritative security enforcement**.

Responsibilities include:

- Evaluating authorization for requested capabilities
- Enforcing access constraints before behavior executes
- Rejecting unauthorized intent explicitly
- Preserving traceability of access decisions

Security decisions made here are definitive. Behavior does not proceed unless authorization succeeds.

---

### Domain Layer

The Domain layer is unaware of security concerns.

Domain logic assumes that any executed behavior has already passed authorization. Introducing security into the domain couples business truth to actor identity and violates separation of concerns.

---

### Infrastructure Layer

The Infrastructure layer supports security mechanisms but does not define access authority.

Responsibilities include:

- Implementing authentication mechanisms
- Enforcing technical security controls
- Protecting system surfaces
- Supporting secure communication

Infrastructure enforces decisions; it does not decide them.

---

## Security at Architectural Boundaries

Security belongs at **system entry points**, where intent first enters the architecture.

Architecturally correct placement ensures that:

- Access decisions are made once
- Execution paths remain explicit
- Authorization failures are predictable
- Responsibility remains centralized

Security must never be interleaved with execution logic.

---

## Consequences of Improper Placement

When security is misplaced:

- Authorization becomes inconsistent
- Behavior becomes conditionally guarded
- Responsibility becomes ambiguous
- Security gaps emerge

Misplaced security transforms protection into risk.

---

## Architectural Rule

> Security is enforced at entry points.  
> Behavior executes only after authorization.

This rule governs all security placement decisions.

---

<p align="center">
  <a href="./01-security-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-security-vs-business-logic.md">Next ▶</a>
</p>
