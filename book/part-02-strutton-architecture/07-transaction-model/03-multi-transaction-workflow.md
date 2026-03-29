# Multi-Transaction Model

Some operations cannot be completed within a single unit of work.

These scenarios require multiple steps that must be coordinated to achieve the desired outcome.

In this model, execution is structured across multiple operations.

Each step may involve separate data interactions, and the system must ensure that these steps are performed in a controlled and predictable way.

This introduces a different execution model.

Instead of treating the request as a single unit, the system treats it as a coordinated workflow.

This is where Orchestration becomes necessary.

The purpose of this model is not complexity.

It is control.

When multiple steps are required, the architecture provides a structured way to manage them without losing clarity.

---

[← Back](02-single-transaction-flow.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-choosing-the-right-approach.md)