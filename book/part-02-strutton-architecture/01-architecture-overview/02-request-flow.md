# Request Flow

Understanding how a request moves through the architecture is essential to understanding how the architectural units work together.

Every request follows a deliberate path through the system. That path is designed to reinforce architectural boundaries, maintain clear responsibilities, and ensure that each architectural unit performs only the work it was designed to own.

A request begins in the **Presentation** layer, where incoming data is received and translated into an application request.

From there, the request enters the **Application** layer, where execution is coordinated. Validation, transformation, business execution, and persistence are performed by the architectural units responsible for those activities. Throughout execution, each architectural unit communicates only through defined contracts while respecting the dependency direction established by the architecture.

As the request moves through the system, interaction models are translated into domain entities. From that point forward, the business execution operates on the domain model rather than the external representation of the data.

Once processing is complete, the result follows the same architectural path in reverse, eventually returning to the Presentation layer where it is translated into the response returned to the client.

This flow is intentional.

Every transition reinforces the architectural principles established throughout this book. Responsibilities remain clearly separated, dependencies move in a controlled direction, and interactions occur only through explicitly defined contracts. Rather than relying solely on developer discipline, the structure of the architecture reinforces the correct flow of execution.

---

[← High-Level Structure](01-high-level-structure.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Key Design Decisions →](03-key-design-decisions.md)