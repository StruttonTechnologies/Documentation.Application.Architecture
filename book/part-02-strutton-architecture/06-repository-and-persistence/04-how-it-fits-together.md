# How It Fits Together

Repository contracts, persistence abstraction, and transaction boundaries work together to preserve the architectural separation between business execution and persistence.

The Application layer interacts only with repository contracts.

Those contracts define the persistence operations available to the architecture while keeping persistence implementations hidden behind the architectural boundary.

Persistence implementations fulfill those operations without exposing their internal details to the rest of the application.

Transaction ownership follows the same architectural responsibilities established throughout the system.

When the Coordinator owns the execution of a request, it owns the transaction boundary.

When Orchestration owns the execution of a workflow, it owns the transaction boundary.

Together, these responsibilities ensure that persistence remains isolated from business execution while allowing data operations to occur in a controlled, predictable, and maintainable manner.

---

[← Commit and Transaction Boundaries](03-commit-and-transaction-boundaries.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Common Architectural Mistakes →](05-common-failure-modes.md)