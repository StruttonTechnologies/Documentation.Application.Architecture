# Configuration Anti-Patterns

## Responsibility

The responsibility of identifying configuration anti-patterns is to ensure that **configuration remains a declarative source of context and does not become a surrogate for behavior, policy, or control flow**.

These anti-patterns describe failure modes where configuration exceeds its architectural role and undermines system clarity.

---

## Why Anti-Patterns Matter

Configuration misuse rarely appears dangerous at first.

It often begins as a convenience and gradually becomes a hidden mechanism for controlling behavior. Over time, this leads to implicit execution paths, environment-specific logic, and fragile systems.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Configuration as Control Flow

**Anti-pattern:**  
Using configuration values to branch execution paths or determine behavior at runtime.

When configuration determines *what happens next*, it is no longer contextual—it is behavioral.

Consequences include:

- Hidden decision-making
- Environment-dependent outcomes
- Reduced traceability
- Implicit logic paths

Control flow belongs to behavior, not configuration.

---

## Configuration as Business Rules

**Anti-pattern:**  
Encoding business rules, thresholds, or policy decisions in configuration.

Business rules are intrinsic to the domain. Moving them into configuration couples business truth to deployment context and bypasses explicit design.

This results in:

- Undocumented rule changes
- Inconsistent enforcement
- Domain logic that cannot be reasoned about in isolation

Rules must be owned by the domain, not externalized as settings.

---

## Configuration as Feature Gating

**Anti-pattern:**  
Using configuration to enable, disable, or alter core business capabilities.

Feature gating through configuration creates multiple implicit versions of the system. Behavior becomes dependent on environment rather than intent.

This leads to:

- Non-deterministic behavior
- Testing gaps
- Operational surprises

Architectural capability must be explicit, not toggled invisibly.

---

## Configuration as Policy Enforcement

**Anti-pattern:**  
Using configuration to approve, deny, or override decisions.

Policy enforcement requires evaluation, context, and authority. Configuration provides none of these.

When configuration is used as policy:

- Decisions lack traceability
- Responsibility becomes unclear
- Policy changes bypass architectural review

Policy belongs to dedicated decision-making layers.

---

## Configuration as Runtime State

**Anti-pattern:**  
Treating configuration as mutable runtime state.

Configuration is not state. It is context.

When configuration changes dynamically during execution:

- Execution paths become unpredictable
- Debugging requires temporal reconstruction
- System behavior becomes unstable

Runtime state must be explicit and observable, not inferred from changing configuration.

---

## Configuration as Integration Logic

**Anti-pattern:**  
Encoding integration behavior or coordination logic into configuration.

When configuration determines message routing, workflow selection, or interaction patterns, architecture becomes implicit and fragile.

Integration logic must be designed and owned explicitly.

---

## Architectural Rule

> If a change in configuration changes behavior,  
> the configuration has become behavior.

This rule is absolute.

---

## Architectural Outcome

When configuration anti-patterns are avoided:

- Behavior remains explicit
- Architecture remains legible
- Responsibility remains clear
- Change remains intentional

Configuration supports the system without controlling it.

---

<p align="center">
  <a href="./03-configuration-vs-behavior.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../validation/README.md">Next ▶</a>
</p>
2311111