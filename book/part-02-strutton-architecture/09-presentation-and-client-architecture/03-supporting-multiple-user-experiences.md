# Supporting Multiple User Experiences

Because the API is independent of the user interface, the system can support multiple types of clients.

These may include web applications, mobile applications, desktop clients, or other systems. As long as they can communicate over HTTP and exchange compatible data, they can use the same underlying application behavior.

This flexibility is a direct result of the architectural separation.

The system does not need to change to support a new user experience. New clients can be introduced without modifying the core application logic.

This prevents duplication.

Instead of implementing the same behavior in multiple front ends, the system provides a single source of behavior that all clients can rely on.

Each client can then focus on the needs of its own user experience while using the same underlying functionality.

---

[← Back](02-ui-as-client.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-why-this-matters.md)