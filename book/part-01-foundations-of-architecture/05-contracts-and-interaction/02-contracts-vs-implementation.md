# Contracts vs Implementation

A contract is not an implementation.

This distinction is critical.

Implementation defines how something works. It contains the logic, behavior, and internal details of a system. Contracts define how something can be used.

Confusing these two leads to architectural problems.

When implementation details are exposed as part of the interaction surface, other parts of the system begin to depend on those details. This creates tight coupling and makes the system harder to change.

A well-defined contract hides implementation.

It exposes only what is necessary for interaction while keeping internal details contained. This allows the implementation to evolve without affecting other parts of the system.

This separation is what allows architecture to remain stable over time.

Contracts provide a stable way to interact, while implementation can change behind that interaction without breaking the system.

---

[← Back](01-what-contracts-are.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-contracts-matter.md)