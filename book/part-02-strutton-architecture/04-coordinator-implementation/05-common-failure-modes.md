# Common Failure Modes

The Coordinator is often given too much responsibility.

One common issue is allowing handlers to contain complex workflows. This makes them harder to understand and blurs the line between simple request handling and orchestration.

Another failure mode is skipping validation or placing it in the wrong layer.

Validation should occur before execution. When it is placed deeper in the system, invalid data may propagate further than intended.

There is also a tendency to allow DTOs to move beyond the Coordinator.

This exposes external data structures to parts of the system that should operate on domain representations, weakening the separation between interaction and execution.

All of these issues reduce clarity.

The Coordinator should remain focused on handling requests, applying validation, and transitioning from interaction to execution.

---

[← Back](04-dto-to-entity-transition.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../05-orchestration/README.md)