# Request Flow

Understanding how a request moves through the system is key to understanding the architecture.

A request begins in the Presentation layer.

The API receives the request and translates it into a command or query. This command or query is defined as part of a contract, not an implementation.

The request is then sent into the Application layer.

A handler in the Coordinator processes the request. At this point, DTOs are still in use. Validation and mapping occur here, and the request is translated into entities that represent the domain.

From this point forward, execution operates on entities.

If the request involves a single transaction, the handler interacts with the persistence layer through repository contracts and commits the result.

If the request involves multiple steps or transactions, the handler delegates to the Orchestration layer. Orchestration coordinates the workflow and manages how those transactions are executed.

The Infrastructure layer performs the actual data operations and commits changes.

The result then flows back through the system, eventually returning to the Presentation layer.

This flow is intentional.

Each step enforces the architectural rules defined in Part 1. Responsibilities remain separated, dependencies follow a controlled direction, and interaction occurs only through defined contracts.

---

[← Back](01-high-level-structure.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-key-design-decisions.md)