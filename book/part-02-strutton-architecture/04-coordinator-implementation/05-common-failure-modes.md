# Common Architectural Mistakes

The Coordinator is sometimes given responsibilities that belong elsewhere in the architecture.

One common mistake is allowing handlers to coordinate complex workflows. As requests become more complicated, this blurs the distinction between request coordination and orchestration, making the architecture more difficult to understand and evolve.

Another mistake is preparing requests outside the Coordinator. Validation and transformation are architectural responsibilities of request coordination. Moving them elsewhere weakens the consistency of request execution and allows interaction concerns to spread throughout the system.

A third mistake is allowing DTOs to move beyond the Coordinator. When interaction models flow deeper into the architecture, the separation between interaction and domain execution begins to erode, increasing coupling between external and internal concerns.

Each of these decisions weakens the architecture by blurring responsibilities and reducing the effectiveness of its architectural boundaries.

The Coordinator exists to coordinate the execution of individual requests, prepare those requests for execution, and transition interaction into domain execution before delegating additional responsibilities where appropriate.

---

[← DTO to Entity Transition](04-dto-to-entity-transition.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Orchestration →](../05-orchestration/README.md)