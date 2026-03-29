# Execution vs Interaction

A well-structured system separates execution from interaction.

Execution is where the system performs its core behavior. It is where business logic, rules, and decisions are made. This is the part of the system that defines what it does.

Interaction is how the system communicates.

It includes receiving input, validating it, transforming it into a usable form, and returning results. It also includes communication with external systems.

When execution and interaction are mixed, problems begin to appear.

External concerns start to influence core logic. Input handling, formatting, and communication details become intertwined with business behavior. This makes the system harder to understand and harder to change.

Separating these concerns keeps the system clean.

Execution remains focused on behavior. Interaction remains focused on communication. Each can evolve independently without introducing unnecessary coupling.

---

[← Back](01-what-boundary-space-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-boundary-space-matters.md)