# DTO to Entity Transition

The transition from DTOs to entities occurs within the Coordinator.

Before this point, the architecture operates on interaction models designed for communication with external consumers. DTOs describe incoming requests and outgoing responses. They exist to support interaction rather than business execution.

Within the Coordinator, those interaction models transition into domain entities.

Entities represent the concepts and behaviors of the domain. They are used for business execution and remain independent of external concerns such as transport, serialization, or presentation.

This transition establishes a clear architectural boundary.

DTOs do not move deeper into the system.

Entities are not exposed outside the system.

Each model exists only within the architectural responsibility for which it was designed.

This separation prevents architectural leakage.

Interaction concerns remain at the boundary of the architecture, while domain execution remains focused on business concepts. Changes to external interaction therefore do not directly affect the internal behavior of the system.

This transition is one of the primary architectural enforcement points within the application.

It preserves the separation between interaction and execution while reinforcing the distinct responsibilities of the Presentation and Application layers.

---

[← Validation and Transformation](03-validation-and-mapping.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Common Architectural Mistakes →](05-common-failure-modes.md)