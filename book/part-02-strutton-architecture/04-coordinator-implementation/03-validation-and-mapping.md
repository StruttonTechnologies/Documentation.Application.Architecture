# Validation and Transformation

Before execution begins, requests must be prepared for execution.

Within the Coordinator, this preparation includes validating incoming interaction and transforming that interaction into forms suitable for the architectural units responsible for execution.

Validation ensures that requests satisfy the expectations required to begin execution. By validating requests before they progress deeper into the architecture, downstream architectural units can assume they are operating on valid input.

Transformation prepares interaction models for execution.

Requests enter the architecture as interaction models designed for communication with external consumers. Before execution begins, those interaction models are transformed into representations appropriate for the domain and the architectural units responsible for fulfilling the request.

This preparation occurs within the Coordinator.

By keeping validation and transformation together at the architectural entry point for execution, the remainder of the system can remain focused on business execution rather than interaction concerns.

The specific transition from interaction models to domain entities is explored in the next section.

---

[← Handlers and Execution](02-handlers-and-execution.md) |
[Table of Contents](../../04-table-of-contents.md) |
[DTO to Entity Transition →](04-dto-to-entity-transition.md)