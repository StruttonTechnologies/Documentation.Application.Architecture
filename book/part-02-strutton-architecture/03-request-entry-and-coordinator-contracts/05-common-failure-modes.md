# Common Failure Modes

Request entry is often not controlled.

One common issue is allowing the Presentation layer to reference implementation assemblies directly. This makes it possible to call execution logic without going through contracts.

Another failure mode is bypassing commands and queries.

Instead of using structured requests, developers may call services directly. This leads to inconsistent patterns and weakens the architecture.

There is also a tendency to mix interaction and execution.

Validation, mapping, and business logic may be performed in the Presentation layer. This breaks the separation of concerns and makes the system harder to maintain.

All of these issues lead to the same outcome.

The architecture becomes inconsistent and difficult to enforce.

Coordinator contracts only provide value when they are consistently used as the entry point into execution.

---

[← Back](04-why-this-matters.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../04-coordinator-implementation/README.md)