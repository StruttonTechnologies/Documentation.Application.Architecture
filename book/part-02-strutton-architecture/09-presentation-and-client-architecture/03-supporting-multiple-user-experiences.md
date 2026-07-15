# Supporting Multiple User Experiences

Because the API is independent of any specific client, the architecture can support multiple user experiences without changing its business behavior.

These clients may include web applications, mobile applications, desktop applications, command-line tools, partner integrations, or future client technologies that have not yet been introduced. As long as they interact through the architectural boundary defined by the API, they can consume the same underlying application behavior.

This flexibility is a direct consequence of the architecture.

Business behavior is implemented once within the application and exposed consistently through the API. New clients can therefore be introduced without modifying the core architecture or duplicating business logic.

This prevents duplication.

Rather than implementing the same business behavior independently for each client, the architecture provides a single source of business behavior that every client can consume.

Each client remains free to provide the user experience most appropriate for its audience while relying on the same underlying application capabilities.

---

[← UI as a Client](02-ui-as-client.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Why This Matters →](04-why-this-matters.md)