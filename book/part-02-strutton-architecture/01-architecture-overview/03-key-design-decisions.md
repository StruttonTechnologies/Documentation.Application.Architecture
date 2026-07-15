# Architectural Principles

The architecture is guided by a small set of architectural principles. Together, these principles shape every architectural unit and every interaction within the system.

## Controlled Visibility

Architectural units expose only the capabilities required by the rest of the system. Implementation details remain hidden behind explicit boundaries, reducing opportunities for unintended coupling.

## Explicit Composition

The application is assembled through a single composition point. This centralizes system assembly while allowing individual architectural units to remain independently responsible for their own implementation.

## Separation of Interaction and Execution

Interaction contracts define how architectural units communicate. Execution remains the responsibility of implementation. This separation allows architectural boundaries to remain stable while implementations evolve independently.

## Separation of External and Domain Models

External interaction models and domain models serve different responsibilities. Separating them prevents external concerns from leaking into the core business model while allowing each to evolve independently.

## Architectural Enforcement

Whenever practical, architectural rules are reinforced through the physical structure of the system rather than relying solely on developer discipline. Controlled dependencies, explicit responsibilities, and limited visibility make the intended architectural path the natural path for developers to follow.

These principles provide the foundation for every architectural unit introduced throughout the remainder of this book. As each chapter explores a specific responsibility, these principles remain the consistent thread that connects the architecture into a cohesive whole.

---

[← Request Flow](02-request-flow.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Application Composition →](../02-application-composition/README.md)