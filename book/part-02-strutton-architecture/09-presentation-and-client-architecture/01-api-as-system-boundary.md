# API as the System Boundary

The API is the architectural boundary of the system.

Every request enters the architecture through the API, and every result leaves through the same boundary. No external consumer interacts directly with the application's internal architectural units.

The API is not a user interface.

Its responsibility is to expose the capabilities of the application to external consumers while remaining separate from both presentation concerns and business execution.

This distinction is intentional.

By treating the API as the architectural boundary, the architecture ensures that every client interacts with the system through a single, consistent entry point. This protects the internal architecture from client-specific concerns while allowing multiple clients to consume the same application behavior.

The API defines how the architecture is accessed.

It does not define how the business behaves.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Clients of the Architecture →](02-ui-as-client.md)