# Common Architectural Mistakes

Orchestration is often introduced when it is not required.

One common mistake is using Orchestration for requests that can be completed through the coordination of a single request. Doing so introduces additional architectural complexity without providing additional architectural value.

Another mistake is allowing the Coordinator to absorb workflow responsibilities. When handlers begin coordinating complex workflows, the distinction between request coordination and workflow coordination gradually disappears, making the architecture more difficult to understand and maintain.

A third mistake is giving Orchestration responsibilities that belong elsewhere. Orchestration coordinates workflows; it does not define business rules, perform persistence operations, or replace the architectural units responsible for those concerns.

Each of these decisions weakens the architecture by blurring responsibilities and reducing the clarity of its architectural boundaries.

Orchestration provides value when it owns only the responsibility for coordinating workflows that extend beyond the scope of a single request.

---

[← How Orchestration Works](04-how-orchestration-works.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Repository and Persistence →](../06-repository-and-persistence/README.md)