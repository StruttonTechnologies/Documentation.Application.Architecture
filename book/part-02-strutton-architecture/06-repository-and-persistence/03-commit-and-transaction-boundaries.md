# Commit and Transaction Boundaries

The architecture explicitly defines where transaction boundaries exist.

Persistence operations may occur throughout the execution of a request or workflow, but changes are committed only at the architectural unit responsible for completing that work. This preserves consistency while ensuring that transaction ownership remains explicit.

For requests coordinated entirely by the Coordinator, the Coordinator owns the transaction boundary.

For workflows coordinated by Orchestration, Orchestration owns the transaction boundary.

This distinction is intentional.

The architectural unit responsible for coordinating the work is also responsible for determining when that work has been completed successfully and when persistence should be committed.

Commit operations are therefore never scattered throughout the architecture.

They occur only at well-defined architectural boundaries, preserving consistency, maintaining data integrity, and reinforcing the ownership of architectural responsibilities.

---

[← Persistence Abstraction](02-persistence-abstraction.md) |
[Table of Contents](../../04-table-of-contents.md) |
[How It Fits Together →](04-how-it-fits-together.md)