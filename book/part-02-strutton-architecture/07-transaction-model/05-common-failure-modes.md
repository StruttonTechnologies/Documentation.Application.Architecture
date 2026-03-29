# Common Failure Modes

Transaction handling is often inconsistent.

One common issue is using Orchestration for simple requests. This introduces unnecessary complexity and makes the system harder to understand.

Another failure mode is handling complex workflows directly in the Coordinator.

This leads to large, difficult-to-maintain handlers and blurs the separation between execution and coordination.

There is also a tendency to lose control of transaction boundaries.

When commits are not clearly defined, it becomes difficult to understand when data changes are finalized. This can lead to inconsistent or unreliable behavior.

All of these issues reduce clarity.

The transaction model only provides value when it is applied consistently and intentionally.

---

[← Back](04-choosing-the-right-approach.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../08-dtos-entities-and-domain-visibility/README.md)