# Security vs Business Logic

## Responsibility

The responsibility of distinguishing security from business logic is to ensure that **access control and protection concerns never become substitutes for domain rules or behavioral decision-making**.

This boundary preserves clarity of authority and prevents security mechanisms from redefining system behavior.

---

## Why the Distinction Matters

Security and business logic serve fundamentally different purposes.

When security logic is allowed to influence business outcomes, authorization decisions become proxies for domain rules, and behavior becomes implicit. The distinction exists to ensure that business behavior remains explicit and authoritative.

This boundary ensures that:

- Access control remains orthogonal to behavior
- Domain rules remain centralized
- Decisions remain traceable
- Behavior remains deterministic

---

## Security

Security determines **who may act**.

Security:

- Evaluates identity and access rights
- Enforces permission boundaries
- Rejects unauthorized intent
- Constrains execution before behavior begins

Security answers the question:

> “Is this actor allowed to attempt this action?”

Security does not determine whether the action is correct or appropriate.

---

## Business Logic

Business logic determines **what is correct within the domain**.

Business logic:

- Expresses domain rules and invariants
- Evaluates correctness based on domain state
- Determines outcomes of valid actions
- Produces success or failure based on rules

Business logic answers the question:

> “Given valid intent, what outcome should occur?”

Business logic is authoritative.

---

## The Boundary Between Them

The architectural boundary is strict.

- Security gates execution
- Business logic governs outcomes
- Security rejects unauthorized actors
- Business logic evaluates authorized actions

If business rules are enforced by security mechanisms, the boundary has been violated.

---

## Authority and Determinism

This distinction preserves authority.

- Security authority ends at access
- Domain authority governs correctness
- Outcomes are produced only by behavior

Blurring these responsibilities introduces hidden policy and undermines architectural trust.

---

## Common Boundary Violations

Typical violations include:

- Authorization rules encoding business thresholds
- Security checks determining success or failure semantics
- Access control used to enforce domain policy
- Conditional business behavior based on actor identity

These patterns replace explicit domain logic with implicit control.

---

## Architectural Rule

> Security determines who may act.  
> Business logic determines what happens.

This separation is non-negotiable.

---

<p align="center">
  <a href="./02-security-placement.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./04-security-anti-patterns.md">Next ▶</a>
</p>
