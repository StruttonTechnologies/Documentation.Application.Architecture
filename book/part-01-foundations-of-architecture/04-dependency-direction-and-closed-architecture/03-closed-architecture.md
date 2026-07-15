# Closed Architecture

A closed architecture is an architecture that enforces its intended structure.

It does this by controlling how responsibilities interact, how dependencies are allowed to flow, and how architectural boundaries are respected. Rather than relying on developer discipline, a closed architecture uses its own structure to prevent incorrect interactions wherever possible.

One of the primary mechanisms used to achieve this is closed layers.

In a closed layered architecture, dependencies are only allowed to flow in a single direction, and each layer may interact only with the layer immediately adjacent to it. Layers cannot bypass one another to access responsibilities that lie beyond their defined boundary.

This prevents architectural shortcuts.

While bypassing layers may appear more efficient in the short term, it weakens the architecture by creating direct dependencies between responsibilities that were intentionally separated. Over time, these shortcuts accumulate, reducing clarity and making change increasingly difficult.

A closed architecture prevents this.

By enforcing dependency direction and preserving architectural boundaries, it ensures that responsibilities remain clearly separated and interactions continue to follow predictable paths.

This is not about limiting flexibility.

It is about preserving architectural integrity.

A closed architecture allows software systems to evolve while maintaining the structure that makes them understandable, maintainable, and predictable.

---

[← Back](02-why-direction-matters.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-common-failure-modes.md)