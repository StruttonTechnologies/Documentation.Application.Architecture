# Common Failure Modes

Application composition is often treated as a convenience rather than a structural concern.

One common issue is centralizing all registration logic in the application entry point. This creates a dependency on every implementation assembly and exposes the entire system to the application layer.

Another failure mode is allowing implementation assemblies to be referenced directly.

This makes it possible to bypass contracts and interact with parts of the system in unintended ways. Over time, this leads to tightly coupled components and a breakdown of architectural boundaries.

There is also a tendency to separate registration from implementation.

When registration logic is not kept close to the code it configures, it becomes harder to maintain. Changes to services may not be reflected in the registration, leading to inconsistencies.

All of these issues weaken the architecture.

ApplicationComposition only provides value when it is treated as a structural mechanism for enforcing boundaries and controlling visibility.

---

[← Back](04-why-this-matters.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../03-request-entry-and-coordinator-contracts/README.md)