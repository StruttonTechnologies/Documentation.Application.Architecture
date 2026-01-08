# Security Anti-Patterns

## Responsibility

The responsibility of identifying security anti-patterns is to ensure that **security remains a protective constraint and does not become a substitute for business logic, orchestration, or architectural intent**.

These anti-patterns describe common failure modes where security concerns exceed their proper scope and undermine clarity, authority, and trust.

---

## Why Anti-Patterns Matter

Security misuse often emerges incrementally.

What begins as a protective measure gradually becomes a mechanism for controlling behavior, encoding policy, or bypassing architectural boundaries. Over time, this results in hidden logic, inconsistent enforcement, and fragile systems.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Security as Business Logic

**Anti-pattern:**  
Encoding domain rules or outcome decisions within security checks.

When security determines whether an action is *correct* rather than whether it is *permitted*, it assumes domain authority.

Consequences include:

- Business rules becoming implicit
- Domain logic losing central ownership
- Authorization outcomes masking true business intent

Security must never evaluate correctness.

---

## Security as Orchestration

**Anti-pattern:**  
Using security mechanisms to coordinate workflows or trigger system behavior.

Security exists to constrain access, not to initiate or sequence actions. When orchestration is embedded in security checks, execution paths become implicit and difficult to reason about.

This leads to:

- Side effects occurring during authorization
- Fragmented execution responsibility
- Untraceable behavior initiation

Security must remain non-behavioral.

---

## Security as Policy Encoding

**Anti-pattern:**  
Encoding business policy directly into security rules.

Policy decisions often require domain context and explicit authority. Embedding them in security mechanisms couples policy to identity and obscures decision ownership.

This results in:

- Undocumented policy changes
- Ambiguous authority
- Policy enforcement that bypasses domain review

Policy must be explicit and architecturally owned.

---

## Security as Conditional Behavior

**Anti-pattern:**  
Altering system behavior based on security outcomes beyond access allowance.

When authorization outcomes influence workflow paths or execution semantics, behavior becomes identity-dependent and implicit.

This introduces:

- Non-deterministic execution
- Testing complexity
- Hidden behavior variants

Security may gate execution, but it must not shape it.

---

## Security as Runtime State

**Anti-pattern:**  
Basing security decisions on mutable or hidden runtime state.

Security decisions must be deterministic and explainable. When access outcomes depend on transient conditions or implicit state, trust erodes.

This leads to:

- Inconsistent authorization results
- Difficult-to-reproduce access failures
- Reduced observability

Security must rely on explicit identity and context.

---

## Architectural Rule

> If security determines outcomes,  
> security has become behavior.

This rule is absolute.

---

## Architectural Outcome

When security anti-patterns are avoided:

- Access control remains explicit
- Authority remains centralized
- Behavior remains intentional
- Architecture remains legible and trustworthy

Security protects the system without redefining it.

---

<p align="center">
  <a href="./03-security-vs-business-logic.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../transactions/README.md">Next ▶</a>
</p>
