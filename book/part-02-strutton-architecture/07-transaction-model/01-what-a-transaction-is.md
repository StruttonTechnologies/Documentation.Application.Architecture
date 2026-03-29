# What a Transaction Is

A transaction represents a unit of work that changes data.

It defines a set of operations that must either complete successfully together or not be applied at all. This ensures that the system remains in a consistent state.

In this architecture, transactions are controlled intentionally.

They are not spread across the system or triggered implicitly. Instead, they are defined as part of the execution flow.

This allows the system to maintain consistency.

By controlling when a transaction begins and when it is committed, the architecture ensures that data changes are applied in a predictable and reliable way.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-single-transaction-flow.md)