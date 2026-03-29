# When Orchestration Is Not Used

Orchestration is not required for every request.

If a request can be completed within a single transaction, the Coordinator handles it directly.

Introducing Orchestration in these cases adds unnecessary complexity.

It creates additional layers of abstraction without providing value. This can make the system harder to understand and maintain.

The goal is not to use Orchestration everywhere.

The goal is to use it only when it is needed.

This keeps the architecture simple where possible and structured where necessary.

---

[← Back](02-when-orchestration-is-used.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-how-orchestration-works.md)