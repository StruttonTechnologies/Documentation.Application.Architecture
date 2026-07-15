# Role of the Coordinator

The Coordinator is responsible for coordinating the execution of incoming requests.

It serves as the architectural entry point for execution within the Application layer. Requests that enter the architecture as commands or queries begin their execution here.

The Coordinator does not contain business rules.

Its responsibility is to coordinate how a request is processed while ensuring that execution follows the architectural structure established throughout the system.

This responsibility includes:

- validating incoming interaction
- transforming interaction models into domain representations
- delegating work to the appropriate architectural units
- returning results to the caller

The Coordinator is intentionally limited in scope.

It does not manage complex workflows or coordinate multiple transactions. Those responsibilities belong to the Orchestration layer, allowing the Coordinator to remain focused on coordinating the execution of individual requests.

By limiting the Coordinator to a single responsibility, the architecture maintains a clear separation between request coordination and workflow orchestration.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Handlers and Execution →](02-handlers-and-execution.md)