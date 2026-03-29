# What Application Composition Is

ApplicationComposition is responsible for assembling the system.

It provides a single entry point for registering all services required by the application while keeping that registration logic organized and controlled.

Instead of placing all registration logic in the application entry point, ApplicationComposition gathers registrations from across the system and combines them into a unified structure.

This separates construction from execution.

The application entry point does not need to understand the internal structure of the system. It delegates that responsibility to ApplicationComposition, which knows how to assemble the application correctly.

ApplicationComposition is a composition concern.

It is allowed to reference implementation assemblies because its role is to build the system, not to participate in its runtime behavior.

This distinction is important.

By isolating composition into a single controlled area, the system can enforce architectural rules without exposing implementation details to the rest of the application.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-distributed-registration.md)