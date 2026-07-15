# Controlled Access to Execution

Execution logic is intentionally hidden from the Presentation layer.

Although every request must ultimately be executed, the Presentation layer never interacts directly with the execution logic responsible for fulfilling that request.

Instead, execution occurs behind the architectural boundary established by the Coordinator contracts.

When a request enters the Application layer, the architecture determines how that request is fulfilled. The Presentation layer neither knows nor needs to know which architectural units participate in the execution process.

This controlled access is fundamental to the architecture.

Without it, execution logic could be accessed directly, architectural boundaries could be bypassed, and tight coupling would gradually replace the intended dependency structure.

By controlling access to execution, the architecture reinforces a single, consistent interaction path. Requests enter through contracts, execution remains behind implementation, and architectural responsibilities remain clearly separated.

---

[← Coordinator Contracts](02-coordinator-contracts.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Why This Matters →](04-why-this-matters.md)