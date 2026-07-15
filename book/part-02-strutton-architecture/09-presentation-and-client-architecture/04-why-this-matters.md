# Why This Matters

Without a clear separation between the architecture and its clients, business behavior gradually spreads beyond the architectural boundaries intended to contain it.

Business logic becomes duplicated across multiple clients. Changes must be implemented in several places. Over time, different clients begin to behave differently, and the architecture loses its consistency.

Separating the API from its clients prevents this.

The architecture owns business behavior.

Clients consume that behavior.

This allows every client to interact with the same application capabilities while remaining free to provide its own user experience.

This separation improves maintainability.

It also improves flexibility.

New clients can be introduced, existing clients can evolve independently, and the architecture continues to expose the same business behavior through a single architectural boundary.

Ultimately, this reinforces the central principle of the architecture.

Each architectural unit remains responsible for the behavior it owns, allowing the system to evolve without responsibilities becoming blurred across architectural boundaries.

---

[← Supporting Multiple User Experiences](03-supporting-multiple-user-experiences.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Common Architectural Mistakes →](05-common-architectural-mistakes.md)