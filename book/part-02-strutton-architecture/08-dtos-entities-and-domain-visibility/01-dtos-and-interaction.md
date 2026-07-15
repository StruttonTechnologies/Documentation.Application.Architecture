# DTOs and Interaction

DTOs exist to support interaction with the outside world.

They define the information exchanged between the architecture and its consumers while remaining independent of the domain model used for business execution.

This distinction is intentional.

The architecture does not expose domain entities directly. Instead, it communicates through DTOs that are designed specifically for interaction. This allows the external representation of data to evolve independently of the internal business model.

Because DTOs exist only to support interaction, they remain at the architectural boundary.

They enter the architecture through the Presentation layer and are prepared for execution within the Application layer before being transformed into domain entities.

DTOs do not represent business concepts.

They represent the information required for interaction, allowing the architecture to protect its internal model while providing stable contracts to external consumers.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Entities and Business Execution →](02-entities-and-execution.md)