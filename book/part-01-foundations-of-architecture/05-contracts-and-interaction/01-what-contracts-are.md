# What Contracts Are

Architectural contracts define how different parts of a system are allowed to interact.

While boundaries separate areas of responsibility and direction controls how dependencies flow, contracts define the terms of interaction between those areas.

A contract specifies how interaction is allowed to occur.

It defines the shape of the interaction without exposing how that interaction is implemented. This allows parts of the system to communicate in a controlled and predictable way, regardless of where that interaction occurs.

Contracts act as constraints.

They limit what can be accessed and how it can be used. This ensures that interaction between parts of the system remains intentional rather than arbitrary.

Without contracts, interaction becomes uncontrolled.

Components may directly depend on internal details of other parts of the system. Over time, this leads to tight coupling and a breakdown of structure.

Contracts prevent this by clearly defining the allowed surface of interaction.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-contracts-vs-implementation.md)