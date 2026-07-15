# Distributed Registration

ApplicationComposition assembles the application, but it does not own the registration of every service.

Instead, registration is distributed.

Each implementation assembly is responsible for registering the services it provides. This keeps configuration close to the code it belongs to, allowing each architectural unit to define its own construction requirements without exposing those details to the rest of the system.

ApplicationComposition gathers these registrations.

Rather than containing every registration itself, it delegates registration to the architectural units responsible for their implementation and then combines those registrations into a complete application.

This creates a structured aggregation.

Individual assemblies own their registrations. Layer-level composition classes aggregate the registrations for their respective layers. ApplicationComposition then combines those layer-level compositions into a single application.

This separation of responsibilities provides a balance between local ownership and centralized assembly. Registration remains close to the code it configures, while application construction remains centralized within the architectural unit responsible for composing the system.

---

[← What Is ApplicationComposition?](01-what-application-composition-is.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Controlled Visibility →](03-controlled-visibility.md)