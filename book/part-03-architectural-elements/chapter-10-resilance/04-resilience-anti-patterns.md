# Resilience Anti-Patterns

## Responsibility

The responsibility of identifying resilience anti-patterns is to ensure that **failure-tolerance mechanisms do not silently alter behavior, outcomes, or architectural intent**.

These anti-patterns describe common failure modes where resilience exceeds its proper scope and undermines predictability, clarity, and trust.

---

## Why Anti-Patterns Matter

Resilience misuse often begins with the desire to “keep things running.”

Over time, mechanisms intended to contain failure become hidden sources of behavior change, implicit recovery, or masked error conditions. When this happens, system behavior becomes environment-dependent and difficult to reason about.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Resilience as Business Logic

**Anti-pattern:**  
Altering business outcomes based on resilience conditions.

When degradation or fallback behavior determines business results, resilience has become business logic.

Consequences include:

- Inconsistent outcomes under failure
- Hidden decision-making
- Loss of domain authority

Resilience must never determine meaning.

---

## Resilience as Control Flow

**Anti-pattern:**  
Using resilience mechanisms to direct execution paths or sequence behavior.

When failure-tolerance logic determines *what happens next*, execution becomes implicit and responsibility becomes unclear.

This results in:

- Hidden branching behavior
- Unpredictable execution paths
- Increased cognitive load

Control flow must remain explicit.

---

## Resilience as Recovery

**Anti-pattern:**  
Embedding corrective or self-healing behavior within resilience mechanisms.

Resilience contains failure; it does not fix it. When recovery is implicit, failure causes remain hidden and behavior becomes opaque.

This leads to:

- Silent failure masking
- Loss of observability
- Delayed diagnosis

Recovery must be explicit and intentional.

---

## Resilience as Error Suppression

**Anti-pattern:**  
Suppressing or hiding errors in the name of availability.

When errors are swallowed to preserve uptime, correctness and trust are sacrificed.

This introduces:

- Silent data corruption
- Misleading system health signals
- Difficult debugging

Errors must remain visible.

---

## Resilience as Environment Dependency

**Anti-pattern:**  
Allowing system behavior to vary based on infrastructure reliability or load.

When outcomes differ depending on failure conditions, behavior becomes non-deterministic.

This results in:

- Environment-specific semantics
- Testing complexity
- Reduced predictability

Behavior must remain stable across conditions.

---

## Architectural Rule

> If resilience changes behavior,  
> resilience has exceeded its role.

This rule is absolute.

---

## Architectural Outcome

When resilience anti-patterns are avoided:

- Failure tolerance remains explicit
- Behavior remains intentional
- Responsibility remains clear
- Architecture remains stable and trustworthy

Resilience protects the system without redefining it.

---

<p align="center">
  <a href="./03-resilience-vs-recovery.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../concurrency/README.md">Next ▶</a>
</p>
