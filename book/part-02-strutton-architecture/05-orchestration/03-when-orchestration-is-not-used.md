# When Orchestration Is Not Used

Orchestration is not required for every request.

If a request can be completed through the execution of a single request without requiring additional workflow coordination, the Coordinator is responsible for handling it directly.

Introducing Orchestration in these situations adds unnecessary complexity.

It introduces additional architectural responsibilities without providing corresponding architectural value. The result is a solution that is more difficult to understand, maintain, and evolve.

The goal is not to use Orchestration whenever it is available.

The goal is to use it only when workflow coordination is genuinely required.

This keeps the architecture simple where possible while introducing additional structure only when the complexity of the workflow justifies it.

---

[← When Orchestration Is Used](02-when-orchestration-is-used.md) |
[Table of Contents](../../04-table-of-contents.md) |
[How Orchestration Works →](04-how-orchestration-works.md)