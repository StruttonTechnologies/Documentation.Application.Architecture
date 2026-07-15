# Entities and Execution

Entities exist to represent the business concepts of the domain.

Unlike DTOs, which are designed for interaction, entities are designed to support business execution. They model the concepts, relationships, and behaviors that define how the system operates.

This distinction is intentional.

Business execution should operate on domain representations rather than interaction models. By separating these responsibilities, the architecture protects its internal business model from changes in external consumers or communication requirements.

Entities remain within the architectural boundaries of the system.

They participate in business execution, persistence, and workflow coordination, but they are never exposed directly outside the architecture.

This separation preserves the integrity of the domain while allowing interaction models and business models to evolve independently.

---

[← DTOs and Interaction](01-dtos-and-interaction.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Domain Visibility →](03-domain-visibility.md)