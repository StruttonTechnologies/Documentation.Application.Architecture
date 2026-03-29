# Architecture in Code

Architecture is not something that exists outside of the codebase.

It is expressed through the code itself.

You can see it in how responsibilities are divided. You can see it in how dependencies flow between components. You can see it in where business logic lives and how different parts of the system interact.

If a system is difficult to understand, the architecture is unclear.

If a system is difficult to change, the architecture is not holding.

There is no hidden layer where architecture lives. It is not something that exists only in diagrams or documentation. It is present in every structural decision made in the code.

This is why architecture cannot be treated as something separate from implementation.

You cannot design a clean architecture and then ignore it in the code. The structure must be reflected consistently in how the system is built.

Every time a responsibility is placed, every time a dependency is introduced, and every time a boundary is crossed, the architecture is either being reinforced or weakened.

---

[← Back](02-where-systems-fail.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-why-architecture-matters.md)