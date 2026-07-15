# Contracts vs Implementation

A contract is not an implementation.

This distinction is fundamental to software architecture.

A contract defines what interaction is permitted.

An implementation defines how that interaction is fulfilled.

Implementation contains the behavior, logic, algorithms, and internal details required to perform work. A contract exposes only the interaction that other parts of the system are allowed to depend upon.

Confusing these two leads to architectural problems.

When implementation details become part of the interaction surface, other responsibilities begin depending on those internal details rather than on the architectural agreement. This creates tight coupling and makes the architecture increasingly difficult to evolve.

A well-defined contract hides its implementation.

It exposes only what is necessary for interaction while keeping internal behavior contained behind the contract. This allows the implementation to change without affecting the responsibilities that depend upon it.

This separation is what allows architecture to remain stable over time.

Contracts provide a stable agreement for interaction.

Implementations remain free to evolve as long as they continue to honor that agreement.

---

[← Back](01-what-contracts-are.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-contracts-matter.md)