# Key Design Decisions

This architecture is built around a set of deliberate design decisions.

These decisions are not arbitrary. They exist to enforce structure and prevent common failure patterns.

## Controlled Visibility

The Presentation layer does not have direct access to implementation assemblies.

It interacts only through contracts and ApplicationComposition. This prevents developers from bypassing architectural boundaries and ensures that all interaction follows the intended structure.

## Composition as a Central Concern

ApplicationComposition is responsible for assembling the system.

Each implementation assembly defines its own service registrations. ApplicationComposition collects these registrations and exposes them as a single unit.

This keeps registration logic close to the code it configures while maintaining a clean entry point for the application.

## Separation of Contracts and Implementation

Contracts are defined separately from implementation.

The API is aware of commands and queries, but not the handlers that execute them. This prevents direct access to execution logic and enforces the use of the intended interaction path.

## Controlled Use of Orchestration

Orchestration is used only when necessary.

If a request can be completed within a single transaction, the Coordinator handles it directly. If multiple steps are required, Orchestration is introduced to manage the workflow.

This avoids unnecessary complexity while still supporting more advanced scenarios.

## DTO and Entity Separation

DTOs are used for interaction.

Entities are used for execution.

The transition between the two occurs within the Coordinator. This ensures that domain concepts are not exposed prematurely and that external concerns do not leak into core logic.

## Architecture as Enforcement

The architecture is designed so that incorrect usage is difficult or impossible.

Developers are not expected to remember the rules. The system enforces them through dependency control and visibility.

This is the defining characteristic of the architecture.

---

[← Back](02-request-flow.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../02-application-composition/README.md)