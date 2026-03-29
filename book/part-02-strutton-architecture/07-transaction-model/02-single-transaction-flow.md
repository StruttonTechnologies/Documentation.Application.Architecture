# Single Transaction Model

The simplest form of execution in this architecture is a single transaction.

In this model, a request results in one unit of work that can be completed without coordination across multiple steps.

This model has clear characteristics:

- all required operations occur within a single execution path  
- changes are applied as one consistent unit  
- no coordination layer is required  

This is the preferred approach when possible.

It keeps execution simple, predictable, and easier to reason about. The architecture does not introduce additional structure unless it is needed.

The key principle is restraint.

Structure is added only when complexity requires it.

---

[← Back](01-what-a-transaction-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-multi-transaction-workflow.md)