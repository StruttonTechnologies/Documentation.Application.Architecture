# Coordinator Contracts

Coordinator contracts define how requests enter the Application layer.

Commands and queries are part of these contracts. They provide a structured way for the Presentation layer to communicate with the system without having access to its internal implementation.

These contracts are visible to the Presentation layer.

This allows the API to create and send requests without knowing how those requests are handled.

The implementation of those requests is not visible.

Handlers, validation, and execution logic exist in implementation assemblies that are not accessible to the Presentation layer.

This separation is intentional.

It ensures that interaction occurs through defined contracts rather than direct access to execution logic.

Coordinator contracts act as the boundary between interaction and execution.

---

[← Back](01-request-entry.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-controlled-access-to-execution.md)