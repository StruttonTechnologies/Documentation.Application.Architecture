# Controlled Access to Execution

Execution logic is not directly accessible from the Presentation layer.

Even though the system must execute requests, that execution is intentionally hidden behind contracts and infrastructure such as MediatR.

When a command or query is sent, the system resolves the appropriate handler internally. The Presentation layer does not know which handler is used or how the request is processed.

This prevents direct access.

Without this control, the Presentation layer could reference handler implementations directly, bypassing architectural boundaries and introducing tight coupling.

By restricting access, the architecture enforces the intended flow.

Requests must pass through contracts, and execution must occur within the Application layer. This ensures that all interaction follows the same controlled path.

---

[← Back](02-coordinator-contracts.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-why-this-matters.md)