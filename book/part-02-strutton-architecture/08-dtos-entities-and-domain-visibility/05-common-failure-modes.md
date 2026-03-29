# Common Failure Modes

DTOs are often allowed to move beyond their intended boundary.

One common issue is using DTOs within execution logic. This mixes interaction concerns with domain behavior and weakens the separation between layers.

Another failure mode is exposing entities externally.

When domain entities are used for communication, internal structures become coupled to external requirements. This makes the system harder to change.

There is also a tendency to bypass mapping.

Skipping the transition between DTOs and entities may seem efficient, but it removes a critical boundary and allows concerns to mix.

All of these issues reduce clarity.

DTOs and entities only provide value when their roles are clearly defined and consistently enforced.

---

[← Back](04-why-this-matters.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../09-presentation-and-client-architecture/README.md)