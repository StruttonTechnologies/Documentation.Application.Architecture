# Domain Visibility Rules

The domain is intentionally hidden from external consumers.

Architectural boundaries exist not only to separate responsibilities, but also to control visibility. The business concepts that define the domain remain internal to the architecture and are never exposed directly outside those boundaries.

The Presentation layer interacts only through DTOs and architectural contracts.

It has no knowledge of domain entities, business behavior, or persistence implementations. This allows external interaction to evolve without directly influencing the internal business model.

This separation protects the domain.

Business concepts remain focused on solving business problems rather than adapting to communication formats, user interface requirements, or external integration concerns.

The Coordinator serves as the architectural boundary where interaction transitions into business execution, but the purpose of that boundary is to preserve domain visibility rather than simply transform data.

The architecture enforces these visibility rules through its physical structure, making incorrect dependencies difficult to introduce rather than relying on developer discipline alone.

---

[← Entities and Execution](02-entities-and-execution.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Why This Matters →](04-why-this-matters.md)