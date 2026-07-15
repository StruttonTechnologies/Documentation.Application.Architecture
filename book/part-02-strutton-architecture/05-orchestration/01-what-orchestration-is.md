# What Orchestration Is

Orchestration is responsible for coordinating multi-step workflows.

While the Coordinator is responsible for coordinating the execution of an individual request, Orchestration is responsible for coordinating work that extends beyond the scope of a single request.

These workflows may involve:

- multiple execution steps
- multiple architectural units
- conditional execution paths
- multiple transactions when required

Orchestration does not define business rules.

Its responsibility is to coordinate how work progresses across multiple steps while preserving the architectural boundaries established throughout the system.

This distinction is fundamental.

The Coordinator coordinates the execution of an individual request.

Orchestration coordinates the execution of an entire workflow.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[When Orchestration Is Used →](02-when-orchestration-is-used.md)