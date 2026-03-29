# Why Boundary Space Matters

Without a clear boundary space, interaction spreads into the system.

At first, this may seem harmless. Input handling, data transformation, and communication logic are added where they are needed. Over time, these concerns begin to mix with core behavior.

This leads to confusion.

It becomes difficult to distinguish between logic that defines behavior and logic that handles interaction. Changes to input or output formats may require changes in core parts of the system. External concerns begin to affect internal behavior.

Boundary space prevents this.

By isolating interaction, it ensures that communication concerns do not interfere with execution. The system remains focused on what it does, while interaction remains controlled and predictable.

This separation makes the system easier to understand and easier to change.

It also makes it easier to adapt.

Changes to how the system interacts with the outside world can be made without affecting how the system behaves internally.

---

[← Back](02-execution-vs-interaction.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-common-failure-modes.md)