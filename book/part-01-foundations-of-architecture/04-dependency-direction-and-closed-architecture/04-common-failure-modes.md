# Common Failure Modes

Dependency direction is often defined but not enforced.

One common issue is allowing dependencies to be introduced in any direction. This typically happens for convenience, when a shortcut seems easier than following the intended structure.

Over time, this leads to tangled dependencies.

Another failure mode is allowing layers to be bypassed.

A component may depend directly on another layer that is not adjacent to it. While this may simplify a specific use case, it breaks the consistency of the architecture and introduces hidden coupling.

There is also a tendency to relax direction rules under pressure.

Deadlines or complexity may lead to decisions that violate the intended structure. These decisions accumulate, gradually eroding the architecture.

All of these issues lead to the same outcome.

The system becomes harder to understand, harder to maintain, and more prone to unintended side effects.

Dependency direction only provides value when it is clearly defined and consistently enforced.

---

[← Back](03-closed-architecture.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../05-contracts-and-interaction/README.md)