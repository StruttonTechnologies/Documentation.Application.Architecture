# Common Failure Modes

Orchestration is often overused.

One common issue is introducing Orchestration for simple requests that could be handled within a single transaction. This adds unnecessary complexity and reduces clarity.

Another failure mode is placing too much logic in the Coordinator.

When complex workflows are handled directly in handlers, they become difficult to understand and maintain. This blurs the separation between execution and coordination.

There is also a tendency to mix responsibilities within Orchestration.

Orchestration should coordinate execution, not define business rules or perform low-level operations. When these responsibilities are mixed, the structure of the system becomes unclear.

All of these issues reduce clarity.

Orchestration provides value when it is used intentionally and only when required.

---

[← Back](04-how-orchestration-works.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../06-repository-and-persistence/README.md)