# Coordinator Contracts

Coordinator contracts define the architectural boundary between interaction and execution.

They provide the only intended entry point into the Application layer, allowing the Presentation layer to describe requests without requiring knowledge of how those requests are executed.

Commands and queries are defined by these contracts. They represent the requests exchanged between the Presentation layer and the Application layer while keeping execution details hidden behind the architectural boundary.

Coordinator contracts are intentionally visible to the Presentation layer.

This allows requests to be created and submitted without exposing the handlers, validation, orchestration, or execution logic responsible for fulfilling them.

This separation is fundamental to the architecture.

Interaction occurs through explicit contracts.

Execution remains hidden behind implementation.

By separating these responsibilities, the architecture preserves controlled visibility while reinforcing the intended flow of execution.

---

[← Request Entry](01-request-entry.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Controlled Access to Execution →](03-controlled-access-to-execution.md)