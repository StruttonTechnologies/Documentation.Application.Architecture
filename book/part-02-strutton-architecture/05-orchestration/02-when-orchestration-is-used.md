# When Orchestration Is Used

Orchestration is used when a request cannot be completed through the execution of a single request alone.

This typically occurs when:

- multiple execution steps must be coordinated
- operations must occur in a specific sequence
- decisions must be made between execution steps
- multiple architectural units participate in fulfilling the request
- multiple transactions are required when appropriate

In these situations, placing all coordination within a single handler would blur responsibilities and make the request more difficult to understand, maintain, and evolve.

Orchestration provides structure.

It separates workflow coordination from the execution of individual requests, allowing each architectural unit to remain focused on the responsibility it owns.

---

[← What Is Orchestration](01-what-orchestration-is.md) |
[Table of Contents](../../04-table-of-contents.md) |
[When Orchestration Is Not Used →](03-when-orchestration-is-not-used.md)