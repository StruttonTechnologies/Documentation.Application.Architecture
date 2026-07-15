# Repository Contracts

Repository contracts define the architectural boundary between business execution and persistence.

They provide the only intended mechanism through which the Application layer interacts with persistent data. Rather than exposing persistence directly, the architecture defines explicit contracts that describe the data operations available to the rest of the system.

These contracts are visible to the Application layer.

This allows the Coordinator and Orchestration layers to request persistence operations without requiring knowledge of how those operations are implemented.

Repository implementations remain hidden.

The Application layer knows what persistence operations are available, but it does not know how those operations are performed. This preserves the architectural boundary between business execution and persistence.

Repository contracts represent intent.

They describe the persistence operations that the architecture allows while leaving implementation details entirely within the Persistence layer.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Persistence Abstraction →](02-persistence-abstraction.md)