# What Stays the Same

The fundamental architecture remains consistent across application styles.

Whether the system is deployed as a clean monolith, organized into business-aligned services, or distributed as microservices, the same principles continue to apply.

Responsibilities still require clear ownership.

Layers still organize technical responsibilities where layered separation is appropriate. Boundaries still protect responsibilities. Dependency direction still controls interaction. Contracts still define the permitted surface of communication.

Interaction and business execution remain separate.

External representations should not become domain models. Internal implementation should not become part of external contracts. Persistence should remain isolated behind explicit responsibilities.

Transaction ownership remains explicit.

The architectural unit coordinating a local request or workflow owns the boundary of the work it can complete. Distribution may narrow that boundary, but it does not remove the need for ownership.

The architecture must still protect itself.

Visibility, dependency control, composition, and explicit contracts remain necessary regardless of the number of deployable units.

Application style changes the physical arrangement of the system.

It does not replace the principles that make the system understandable.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Changes →](02-what-changes.md)
