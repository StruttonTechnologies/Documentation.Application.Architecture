# Observability Anti-Patterns

## Responsibility

The responsibility of identifying observability anti-patterns is to ensure that **mechanisms intended to provide insight do not evolve into mechanisms that influence, direct, or distort system behavior**.

These anti-patterns describe common failure modes where observability exceeds its architectural role and undermines clarity, determinism, and trust.

---

## Why Anti-Patterns Matter

Observability misuse often begins with good intentions.

Instrumentation added for diagnosis or insight can gradually become entangled with execution, timing, or decision-making. When this occurs, the system’s behavior becomes dependent on being observed, and insight can no longer be trusted.

Anti-patterns exist to make these failures explicit and prevent architectural erosion.

---

## Observability as Control Logic

**Anti-pattern:**  
Using observability signals to influence execution paths or decisions.

When monitoring data determines *what happens next*, observability has become control.

Consequences include:

- Behavior that changes under observation
- Feedback loops that obscure intent
- Execution paths that are difficult to reason about

Observability must never direct behavior.

---

## Observability as Orchestration

**Anti-pattern:**  
Triggering workflows or coordinating actions based on observability mechanisms.

Observability exists to record behavior, not to initiate or sequence it. When orchestration logic is embedded in observability, responsibility becomes implicit and execution opaque.

This results in:

- Hidden coupling between monitoring and behavior
- Unclear execution ownership
- Difficult-to-debug interactions

Orchestration must remain explicit and intentional.

---

## Observability as Error Handling

**Anti-pattern:**  
Using observability mechanisms to suppress, retry, or compensate for failures.

Observability records failure; it does not respond to it. When failure handling is embedded in observability, error semantics become unclear and recovery becomes implicit.

This introduces:

- Hidden retries
- Masked failures
- Distorted failure signals

Error handling must remain explicit and architecturally owned.

---

## Observability as Performance Gatekeeping

**Anti-pattern:**  
Conditioning behavior on observed performance metrics.

When execution paths change based on latency, load, or monitoring thresholds, behavior becomes environment-dependent and non-deterministic.

This leads to:

- Timing-sensitive behavior
- Testing complexity
- Unpredictable outcomes

Performance insight must inform design, not control execution.

---

## Observability as Domain Knowledge

**Anti-pattern:**  
Encoding business meaning or domain interpretation into observability data.

Observability should reflect behavior, not reinterpret it. When domain meaning is inferred or encoded in observability mechanisms, authority shifts away from the domain.

This results in:

- Ambiguous responsibility
- Misleading insight
- Loss of domain clarity

Domain meaning must remain explicit and authoritative.

---

## Architectural Rule

> If observability changes behavior,  
> observability has become control.

This rule is absolute.

---

## Architectural Outcome

When observability anti-patterns are avoided:

- Insight remains trustworthy
- Behavior remains intentional
- Responsibility remains clear
- Architecture remains legible and stable

Observability illuminates the system without reshaping it.

---

<p align="center">
  <a href="./03-observability-vs-control.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../resilience/README.md">Next ▶</a>
</p>
