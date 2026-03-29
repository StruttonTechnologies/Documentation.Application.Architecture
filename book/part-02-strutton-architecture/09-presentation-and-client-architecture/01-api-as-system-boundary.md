# API as the System Boundary

In this architecture, the API represents the boundary of the system.

It is the point where requests enter and results leave. All external interaction passes through the API before reaching the application.

The API is not the user interface.

It exists as its own assembly and is responsible for handling communication with clients. Its role is to receive input, translate that input into requests the system can process, and return the results produced by the system.

This separation is intentional.

By treating the API as the system boundary, the architecture ensures that all interaction follows a consistent path. It also prevents user interface concerns from becoming mixed with application behavior.

The API defines how the system is accessed, not how it behaves.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-ui-as-client.md)