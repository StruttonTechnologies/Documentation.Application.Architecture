# Common Architectural Mistakes

Persistence responsibilities are often placed in the wrong architectural units.

One common mistake is allowing the Application layer to access persistence implementations directly. Doing so bypasses repository contracts, weakens architectural boundaries, and exposes implementation details that should remain hidden.

Another mistake is scattering transaction ownership throughout the application. When multiple architectural units determine when persistence is committed, transaction boundaries become difficult to understand and architectural ownership becomes unclear.

A third mistake is allowing persistence responsibilities to become mixed with business execution responsibilities. When business execution begins managing persistence details, the separation between execution and persistence gradually disappears.

Each of these decisions weakens the architecture by blurring responsibilities and reducing the effectiveness of its architectural boundaries.

Repository contracts and persistence abstractions provide value only when persistence remains the responsibility of the architectural units designed to own it.

---

[← How It Fits Together](04-how-it-fits-together.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Transaction Model →](../08-dtos-entities-and-domain-visibility/README.md)