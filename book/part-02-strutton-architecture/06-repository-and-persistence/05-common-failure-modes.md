# Common Failure Modes

Data access is often implemented without proper abstraction.

One common issue is allowing direct access to the persistence layer. This bypasses repository contracts and exposes implementation details to the rest of the system.

Another failure mode is scattering commit operations.

When commits occur in multiple places, it becomes difficult to understand when changes are finalized. This can lead to inconsistent data and unintended side effects.

There is also a tendency to mix persistence logic with execution logic.

When data access is embedded directly within application logic, it becomes harder to maintain and understand the system.

All of these issues weaken the architecture.

Repository contracts and controlled persistence only provide value when they are consistently applied.

---

[← Back](04-how-it-fits-together.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../07-transaction-model/README.md)