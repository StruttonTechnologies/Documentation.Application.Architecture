# Domain Visibility Rules

Domain concepts are not visible at the system boundary.

The Presentation layer does not have access to domain entities. It interacts only with DTOs and contracts.

This enforces separation.

By restricting visibility, the architecture prevents external concerns from depending on internal structures. It also prevents domain concepts from being shaped by external requirements.

The transition occurs within the Coordinator.

DTOs are mapped to entities, and from that point forward, execution operates on domain representations.

This creates a clear boundary.

Before the Coordinator, interaction occurs through DTOs. After the Coordinator, execution occurs through entities.

This rule is enforced by the structure of the system.

---

---

[← Back](02-entities-and-execution.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-why-this-matters.md)