# Common Architectural Mistakes

Request entry is sometimes treated as a convenience rather than an architectural responsibility.

One common mistake is allowing the Presentation layer to reference implementation assemblies directly. Doing so makes it possible to bypass the intended architectural entry point and interact directly with execution logic.

Another mistake is allowing requests to enter the Application layer through multiple paths. When different parts of the system use different interaction patterns, the architecture gradually loses consistency and becomes more difficult to understand.

A third mistake is exposing execution details instead of interaction contracts. When implementation becomes visible outside the architectural boundary, coupling increases and architectural responsibilities become blurred.

Each of these decisions weakens the architecture by reducing controlled visibility and allowing architectural boundaries to be bypassed.

Coordinator contracts exist to prevent these problems by defining a single, consistent architectural entry point through which every request enters the Application layer.

---

[← Why This Matters](04-why-this-matters.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Coordinator Implementation →](../04-coordinator-implementation/README.md)