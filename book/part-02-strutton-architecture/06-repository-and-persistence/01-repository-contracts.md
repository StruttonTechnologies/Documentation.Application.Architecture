# Repository Contracts

Repository contracts define how the system interacts with data.

They provide a controlled way to access and modify persistence without exposing implementation details. Instead of allowing direct access to the persistence layer, the system interacts through defined contracts.

These contracts are visible to the Application layer.

This allows the Coordinator and Orchestration layers to perform data operations without knowing how those operations are implemented.

The implementation of these contracts is not visible.

This separation ensures that data access follows the architectural rules. Interaction with persistence occurs through a controlled interface rather than direct dependency.

Repository contracts represent intention.

They define what data operations are allowed, not how those operations are performed.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-persistence-abstraction.md)