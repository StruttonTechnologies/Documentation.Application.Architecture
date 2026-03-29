# Commit and Transaction Boundaries

Transactions are controlled through defined boundaries.

Data operations may occur in multiple steps, but changes are not finalized until a commit occurs. This ensures that the system maintains consistency.

The architecture defines where commits are allowed.

In simple cases, a single transaction is handled directly by the Coordinator. Data is modified through repository contracts, and the changes are committed as a single operation.

In more complex cases, Orchestration coordinates multiple steps.

It ensures that all required operations are completed before committing the final result. This allows the system to manage more complex workflows while maintaining consistency.

Commit operations are not scattered throughout the system.

They are controlled and intentional, ensuring that data integrity is maintained.

---

[← Back](02-persistence-abstraction.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-how-it-fits-together.md)