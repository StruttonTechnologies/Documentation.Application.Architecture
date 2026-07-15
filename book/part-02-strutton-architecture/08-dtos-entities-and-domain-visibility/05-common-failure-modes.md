# Common Architectural Mistakes

Interaction and domain representations are often allowed to cross architectural boundaries.

One common mistake is allowing DTOs to move beyond the architectural boundary where they belong. When interaction models participate directly in business execution, the separation between interaction and execution gradually disappears.

Another mistake is exposing domain entities outside the architecture. When business representations become part of external contracts, the internal business model begins to evolve in response to external requirements rather than business requirements.

A third mistake is bypassing the architectural boundary between interaction and business execution. Whether that boundary is crossed through mapping or another transformation mechanism is an implementation detail. What matters architecturally is that the transition occurs at a well-defined boundary.

Each of these decisions weakens the architecture by allowing one representation to assume responsibilities intended for another.

Interaction models and domain models provide value only when each remains responsible for the architectural purpose for which it was designed.

---

[← Why This Matters](04-why-this-matters.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Presentation and Client Architecture →](../09-presentation-and-client-architecture/README.md)
