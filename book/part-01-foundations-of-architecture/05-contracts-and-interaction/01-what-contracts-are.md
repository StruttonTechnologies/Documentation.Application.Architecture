# What Contracts Are

Architectural contracts define how responsibilities within a system are allowed to interact.

Architectural layers organize responsibilities. Architectural boundaries protect those responsibilities. Dependency direction controls how responsibilities are allowed to interact. Architectural contracts regulate that interaction by defining the agreements each responsibility exposes to the rest of the system.

A contract defines the terms of interaction.

It specifies what interaction is allowed without exposing how that interaction is implemented. This allows different responsibilities to communicate in a controlled and predictable manner while remaining independent of each other's internal implementation.

Architectural contracts act as constraints.

They define the public surface through which interaction is permitted while hiding internal implementation details. This limits what can be accessed, how it can be used, and how responsibilities are allowed to communicate.

Without architectural contracts, interaction gradually becomes uncontrolled.

Responsibilities begin depending directly on one another's internal implementation rather than on clearly defined agreements. Over time, this creates tight coupling, weakens architectural boundaries, and gradually erodes the structure of the system.

Architectural contracts prevent this by defining the only approved surface through which interaction may occur.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-contracts-vs-implementation.md)