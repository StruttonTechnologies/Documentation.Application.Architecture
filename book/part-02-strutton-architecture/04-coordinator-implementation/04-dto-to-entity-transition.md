# DTO to Entity Transition

The transition from DTOs to entities occurs within the Coordinator.

Before this point, the system operates on data structures designed for interaction. DTOs represent incoming requests and outgoing responses. They are shaped for communication, not execution.

Within the Coordinator, DTOs are mapped to entities.

Entities represent domain concepts and are used for execution. They carry meaning within the system and are not tied to external concerns such as transport or formatting.

This creates a clear boundary.

DTOs do not move deeper into the system. Entities are not exposed externally. Each is used only in the context where it is appropriate.

This separation prevents leakage.

External concerns remain at the boundary of the system, and internal behavior remains focused on domain concepts. Changes to how data is received or returned do not affect how the system behaves internally.

This transition is one of the most important enforcement points in the architecture.

It ensures that interaction and execution remain distinct and that the system maintains a clear separation of responsibilities.

---

[← Back](03-validation-and-mapping.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](05-common-failure-modes.md)