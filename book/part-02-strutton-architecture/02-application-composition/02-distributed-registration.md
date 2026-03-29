# Distributed Registration

In this architecture, registration is distributed.

Each implementation assembly is responsible for registering its own services. This keeps configuration close to the code it relates to, making it easier to maintain and understand.

ApplicationComposition gathers these registrations.

Instead of writing all registration logic in a single place, ApplicationComposition calls into each layer and collects the service registrations defined by each assembly.

This creates a structured aggregation.

Each layer has its own composition class that combines the registrations of its assemblies. ApplicationComposition then combines those layer-level collections into a single service collection.

This approach provides balance.

Registration is defined locally, where the code exists, but composed centrally, where the application is assembled.

---

[← Back](01-what-application-composition-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-controlled-visibility.md)