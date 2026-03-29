# Handlers and Execution

Handlers are responsible for executing commands and queries.

Each request has a corresponding handler that defines how that request is processed. The handler contains the logic required to fulfill the request within the boundaries of the architecture.

Handlers operate within the Coordinator implementation.

They are not visible to the Presentation layer and cannot be accessed directly. This ensures that all execution follows the intended request flow.

A handler performs the following steps:

- receives the request  
- validates input where necessary  
- maps DTOs into entities  
- performs the required operations  
- returns a result  

Handlers are focused on a single request.

They do not coordinate multiple workflows or manage complex execution paths. This keeps them simple and predictable.

When a request requires more complex behavior, the handler delegates to the Orchestration layer.

---

[← Back](01-role-of-the-coordinator.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-validation-and-mapping.md)