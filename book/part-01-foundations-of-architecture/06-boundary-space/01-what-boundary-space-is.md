# What Boundary Space Is

Boundary space is the area of a system where interaction occurs.

While layers organize responsibility and boundaries separate those responsibilities, boundary space defines where communication happens between different parts of the system and between the system and the outside world.

Not all parts of a system are responsible for executing core behavior.

Some parts exist primarily to receive input, transform it, and pass it into the system. Others exist to take results from the system and present them externally. These areas are part of the boundary space.

Boundary space is distinct from execution space.

Execution space contains the logic that defines how the system behaves. Boundary space contains the logic that defines how the system interacts.

This distinction allows the system to remain focused.

Execution logic remains centered on behavior, while interaction logic is handled separately. This prevents external concerns from spreading into the core of the system.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-execution-vs-interaction.md)