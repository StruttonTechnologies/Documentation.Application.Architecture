# UI as a Client

User interfaces are clients of the system.

They are responsible for collecting input from users and displaying results, but they do not contain application behavior. Instead, they communicate with the system through the API.

This keeps responsibilities clear.

The system owns behavior. The user interface owns presentation.

By separating these concerns, the architecture prevents business logic from being duplicated across different user experiences. The same system can support multiple interfaces without reimplementing core functionality.

This also simplifies development.

User interfaces can focus on experience and interaction, while the system remains focused on execution and behavior.

---

[← Back](01-api-as-system-boundary.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-supporting-multiple-user-experiences.md)