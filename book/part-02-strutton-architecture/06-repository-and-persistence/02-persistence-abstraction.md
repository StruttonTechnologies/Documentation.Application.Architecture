# Persistence Abstraction

Persistence is intentionally separated from business execution through abstraction.

The Application layer does not interact directly with persistence implementations. Instead, it depends on repository contracts that define the persistence operations available to the architecture.

This abstraction preserves architectural responsibilities.

Business execution remains focused on business behavior, while persistence remains focused on storing and retrieving information. Each responsibility can evolve independently without affecting the other.

Abstraction also protects the architecture from implementation details.

Changes to persistence implementations do not require changes to the Application layer, provided the repository contracts continue to represent the same architectural intent.

Abstraction does not remove responsibility.

It ensures that responsibility remains owned by the architectural unit designed to fulfill it.

---

[← Repository Contracts](01-repository-contracts.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Commit and Transaction Boundaries →](03-commit-and-transaction-boundaries.md)