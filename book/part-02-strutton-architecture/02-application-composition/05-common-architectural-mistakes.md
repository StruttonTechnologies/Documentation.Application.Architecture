# Common Architectural Mistakes

Application composition is sometimes treated as a startup convenience rather than an architectural responsibility.

One common mistake is centralizing every service registration in the application entry point. Doing so creates unnecessary knowledge of implementation assemblies and gradually weakens architectural boundaries.

Another mistake is allowing implementation assemblies to be referenced directly by other architectural units. This bypasses the intended interaction paths, encourages unintended dependencies, and increases coupling throughout the system.

A third mistake is separating registration from the implementation it configures. When registration is maintained independently from the code it supports, the two can easily drift apart, making the system more difficult to understand and maintain.

Each of these decisions appears reasonable in isolation. Over time, however, they contribute to architectural drift by weakening controlled visibility, increasing coupling, and reducing the effectiveness of the architectural boundaries established by the system.

ApplicationComposition exists to prevent these problems by treating application composition as an architectural responsibility rather than a startup concern.

---

[← Why This Matters](04-why-this-matters.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Request Entry and Coordinator Contracts →](../03-request-entry-and-coordinator-contracts/README.md)