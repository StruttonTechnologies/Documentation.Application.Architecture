# What Service-Based Architecture Is

A service-based architecture organizes a system into independent modules.

Each module represents a group of related functionality and contains its own internal structure. These modules exist within a single deployable application but are treated as separate areas of responsibility.

The architecture itself does not change.

Layers, boundaries, contracts, and controlled interaction still apply. The difference is how those concepts are organized.

Instead of a single unified structure, the system is divided into multiple modules, each with its own internal boundaries.

Modules do not directly interact with the internal implementation of other modules.

Interaction occurs through defined contracts, ensuring that boundaries are respected even within a single application.

This creates a system that is both cohesive and modular.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-how-it-differs-from-a-clean-monolith.md)