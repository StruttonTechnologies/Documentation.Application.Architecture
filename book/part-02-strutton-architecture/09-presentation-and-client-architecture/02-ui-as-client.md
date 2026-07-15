# UI as a Client

User interfaces are one type of client of the architecture.

Their responsibility is to collect interaction from users and present the results returned by the application. They do not own business behavior. Instead, they consume that behavior through the API, which serves as the architectural boundary of the system.

This separation preserves architectural responsibilities.

The application owns business behavior.

The user interface owns presentation and user experience.

Because those responsibilities remain separate, multiple client applications can provide entirely different user experiences while relying on the same underlying business behavior. Business logic is implemented once within the architecture rather than duplicated across individual clients.

This separation also simplifies development.

Each architectural unit remains focused on the responsibility it owns, allowing client applications to evolve independently without affecting business execution.

---

[← API as the System Boundary](01-api-as-system-boundary.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Supporting Multiple User Experiences →](03-supporting-multiple-user-experiences.md)