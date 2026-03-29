# Persistence Abstraction

Persistence is abstracted from execution.

The system does not interact directly with the underlying data store. Instead, it relies on contracts that define how data operations are performed.

This abstraction separates concerns.

Execution logic focuses on behavior, while persistence logic focuses on data storage and retrieval. Each can evolve independently without affecting the other.

This also protects the system from implementation details.

Changes to the persistence mechanism do not require changes in the Application layer, as long as the contracts remain consistent.

Abstraction does not remove responsibility.

It ensures that responsibility is placed in the correct part of the system.

---

[← Back](01-repository-contracts.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-commit-and-transaction-boundaries.md)