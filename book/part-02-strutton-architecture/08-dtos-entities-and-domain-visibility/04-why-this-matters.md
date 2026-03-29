# Why This Matters

Without separation between DTOs and entities, concerns begin to mix.

External data structures may start to influence domain logic. Changes to input or output formats can impact core behavior. Over time, this leads to tightly coupled systems that are difficult to maintain.

Separating DTOs and entities prevents this.

It allows the system to evolve independently in terms of interaction and execution. Changes to how data is received or returned do not affect how the system behaves internally.

This improves flexibility.

It also improves clarity.

Each part of the system operates within its intended responsibility.

---

[← Back](03-domain-visibility-rules.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](05-common-failure-modes.md)