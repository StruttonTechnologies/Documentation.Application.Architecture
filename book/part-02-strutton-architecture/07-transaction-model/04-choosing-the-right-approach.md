# Choosing the Right Model

The architecture defines two valid ways to handle data changes.

A request should follow the simplest model that satisfies its requirements.

If the operation can be completed as a single unit of work, the single transaction model should be used.

If the operation requires multiple coordinated steps, the multi-transaction model should be used.

This decision is not arbitrary.

It is based on the nature of the work being performed.

Choosing the correct model is critical.

Using a multi-transaction approach for simple operations introduces unnecessary complexity. Using a single transaction approach for complex workflows leads to unclear and fragile execution.

The architecture provides both options.

It is the responsibility of the system to apply them appropriately.

---

[← Back](03-multi-transaction-workflow.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](05-common-failure-modes.md)