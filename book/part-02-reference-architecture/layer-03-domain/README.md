# Section — Domain Layer

The Domain Layer contains the business concepts, rules, and invariants that define the
problem space the application exists to serve.

This layer represents the *core meaning* of the system. It is independent of user
interfaces, application workflows, and technical infrastructure.

---

## Purpose of the Domain Layer

The purpose of the Domain Layer is to:

- Express business concepts and terminology
- Enforce business rules and invariants
- Protect business integrity over time

The Domain Layer exists to ensure that business logic remains correct regardless of how
the application is accessed or implemented.

---

## What Belongs in the Domain Layer

The Domain Layer may contain:

- Entities and value objects
- Domain services
- Business rules and invariants
- Domain events
- Domain-specific contracts

All logic in this layer should be directly related to business meaning.

---

## What Does Not Belong in the Domain Layer

The Domain Layer must not contain:

- Application orchestration or workflows
- UI or transport concerns
- Persistence or infrastructure logic
- Framework-specific dependencies
- Knowledge of how the application is executed

If logic depends on *when* or *how* something is invoked, it does not belong here.

---

## Dependency and Visibility Rules

The Domain Layer:

- Has no dependencies on other layers
- Defines contracts that other layers depend on
- Is not aware of application workflows or infrastructure details

This independence ensures that business logic remains stable even as the surrounding
system evolves.

---

## Business Integrity as a Primary Concern

The Domain Layer is the final authority on business correctness.

Application behavior must conform to domain rules, not the other way around. By isolating
these rules, the architecture prevents business logic from being diluted or bypassed
by technical concerns.

---

## Preparing for the Infrastructure Layer

While the Domain Layer defines *what must be true*, it does not concern itself with *how*
those truths are persisted, communicated, or integrated.

The next section introduces the Infrastructure Layer and explains how technical concerns
are isolated without leaking into the core of the system.

---

<p align="center">
  <a href="../section-application-layer/README.md">◀ Previous Section</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../section-infrastructure-layer/README.md">Next Section ▶</a>
</p>
