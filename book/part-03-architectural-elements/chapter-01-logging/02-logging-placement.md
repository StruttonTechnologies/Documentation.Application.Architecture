# Logging Placement

## Responsibility

The responsibility of logging placement is to ensure that **observability aligns with architectural boundaries**.

Logging must exist where technical and execution context is available, and must be absent where such context would compromise architectural purity.

Correct placement ensures that logs enhance understanding without introducing coupling.

---

## Why Placement Matters

Logging is cross-cutting, but it is not boundaryless.

When logging is placed indiscriminately, it becomes easy for layers to learn too much about each other. This creates hidden dependencies and makes refactoring risky, as behavior becomes implicitly tied to instrumentation.

Explicit placement rules exist to preserve:

- Separation of concerns
- Dependency direction
- Layer autonomy
- Architectural clarity

---

## Placement by Layer

### Presentation Layer

Logging in the Presentation layer focuses on **interaction boundaries**.

Appropriate logging includes:

- Request receipt and completion
- Transport-level failures
- Authentication and authorization failures
- Input shape validation errors

Presentation logging captures *who called the system and what happened at the boundary*, not how the application responded internally.

---

### Application Layer

Logging in the Application layer focuses on **execution intent and coordination**.

Appropriate logging includes:

- Use-case start and completion
- Handler execution boundaries
- Orchestration progress and failure context
- Application-level exceptions

Application logs describe *what the system attempted to do* and *whether it succeeded*, without embedding business rules.

---

### Domain Layer

The Domain layer does not contain logging.

This is intentional.

Domain logic must remain:

- Deterministic
- Side-effect free
- Independent of infrastructure concerns

Introducing logging into the Domain would couple business rules to technical implementation details and violate the architecture’s dependency direction.

Domain behavior is understood through outcomes, not instrumentation.

---

### Infrastructure Layer

Logging in the Infrastructure layer focuses on **technical execution**.

Appropriate logging includes:

- Persistence failures
- Transaction and connection issues
- External system interactions
- Resource availability and timeouts

Infrastructure logs provide visibility into *how* the system interacts with its environment, without surfacing implementation detail to higher layers.

---

## Cross-Layer Considerations

Some logging concerns span multiple layers, such as:

- Correlation identifiers
- Trace context
- Request identifiers

These concerns must be **passed through**, not interpreted or generated arbitrarily by each layer.

Logging context may flow across layers, but logging behavior must remain localized.

---

## Architectural Outcome

When logging placement is respected:

- Each layer remains independently understandable
- Logs reflect architectural intent
- Changes in one layer do not ripple through others
- Observability improves without compromising design

Logging becomes a tool for clarity rather than a source of complexity.

---

<p align="center">
  <a href="./01-logging-boundaries.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-logging-lifecycle.md">Next ▶</a>
</p>
