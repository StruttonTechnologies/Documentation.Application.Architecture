# Where It Gets More Complex

A service-based architecture introduces additional structure.

While this improves organization, it also introduces new challenges.

Boundaries become more important.

Modules must not depend on each other’s internal implementation. This requires clear contracts and disciplined interaction.

Composition becomes more critical.

The system must be assembled in a way that respects module boundaries while still allowing the application to function as a whole.

Read and write concerns may also become more complex.

As modules become more independent, accessing data across module boundaries requires careful handling to avoid breaking architectural rules.

This added complexity is intentional.

It is introduced to control growth and maintain clarity as the system expands.

The goal is not to eliminate complexity.

The goal is to manage it.

---

[← Back](03-why-modules-matter.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../04-microservices/README.md)