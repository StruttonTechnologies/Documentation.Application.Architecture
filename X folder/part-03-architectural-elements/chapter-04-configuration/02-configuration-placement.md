# Configuration Placement

## Responsibility

The responsibility of configuration placement is to ensure that **contextual values are applied at architectural boundaries without leaking into behavioral execution paths**.

Placement determines whether configuration remains a compositional concern or becomes an implicit source of logic. Correct placement preserves clarity, determinism, and architectural integrity.

---

## Why Placement Matters

Configuration is inherently cross-cutting, but it must not be ubiquitous.

Without explicit placement rules, configuration values are pulled directly into behavioral layers, where they begin to influence decisions, branch execution paths, and bypass architectural intent.

Placement boundaries exist to ensure that:

- Configuration informs composition, not behavior
- Context is applied consistently
- Logic remains explicit and centralized
- Architectural layers retain clear responsibility

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not own configuration.

Presentation concerns may surface configurable limits or display environment-specific values, but they must not interpret or enforce configuration meaning. Configuration does not belong to user interaction logic.

Presentation expresses intent; it does not contextualize it.

---

### Application Layer

The Application layer consumes configuration for **composition and coordination**, not for decision-making.

Configuration may inform:

- Workflow composition
- Capability availability
- Operational constraints

The Application layer must not branch business behavior based on configuration. Decisions remain explicit and input-driven.

---

### Domain Layer

The Domain layer is entirely unaware of configuration.

Domain logic operates solely on:

- Explicit inputs
- Invariants
- Rules intrinsic to the domain

Introducing configuration into the Domain layer couples business truth to environment and violates architectural independence.

---

### Infrastructure Layer

The Infrastructure layer binds configuration to technical mechanisms.

Responsibilities include:

- Applying configuration to technical capabilities
- Adapting external systems to architectural needs
- Enforcing non-behavioral operational constraints

Infrastructure implements configuration; it does not interpret it.

---

## Configuration at Architectural Boundaries

Configuration belongs at the **edges of the system**, where composition occurs.

Architecturally correct placement ensures that:

- Configuration is resolved before execution
- Behavioral layers remain context-agnostic
- Execution paths remain explicit
- Change remains localized

Configuration may be read broadly, but it must be applied narrowly.

---

## Consequences of Improper Placement

When configuration is misplaced:

- Domain logic becomes environment-dependent
- Behavior varies implicitly
- Testing requires environmental replication
- Architecture becomes fragile and opaque

Misplaced configuration transforms context into control.

---

## Architectural Rule

> Configuration is applied at boundaries.  
> Behavior executes within boundaries.

This rule governs all configuration placement decisions.

---

<p align="center">
  <a href="./01-configuration-responsibility.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-configuration-vs-behavior.md">Next ▶</a>
</p>
