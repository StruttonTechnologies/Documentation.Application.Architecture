# Handlers and Execution

Handlers are responsible for executing individual commands and queries.

Each request has a corresponding handler that defines how that request is fulfilled within the architectural boundaries established by the Coordinator. A handler owns the execution of a single request while remaining focused on that request alone.

Handlers exist within the Coordinator implementation.

They are not visible outside the Application layer and cannot be accessed directly by the Presentation layer. Every request must therefore enter through the Coordinator contracts before reaching its handler.

A handler is responsible for:

- receiving a request
- validating the request where appropriate
- transforming interaction models into domain representations
- delegating work to the appropriate architectural units
- returning the result of the request

Handlers are intentionally limited in scope.

Each handler is responsible for a single request. It does not coordinate multiple workflows or manage complex execution paths. When execution extends beyond a single request, responsibility is delegated to the Orchestration layer.

---

[← Role of the Coordinator](01-role-of-the-coordinator.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Validation and Transformation →](03-validation-and-mapping.md)