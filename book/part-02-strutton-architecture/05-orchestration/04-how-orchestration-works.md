# How Orchestration Works

When a request requires Orchestration, the Coordinator delegates responsibility for the workflow.

Rather than coordinating every execution step itself, the Coordinator invokes the Orchestration layer through its contracts. This preserves the separation between request coordination and workflow coordination.

The Orchestration layer then coordinates the workflow.

It determines how the workflow progresses, invokes the architectural units responsible for each step, and ensures that execution follows the intended sequence.

Depending on the workflow, this may involve:

- coordinating multiple execution steps
- invoking multiple architectural units
- managing intermediate state
- coordinating multiple transactions when required

Each responsibility remains clearly defined.

The Coordinator remains responsible for coordinating the execution of an individual request.

The Orchestration layer remains responsible for coordinating the workflow that fulfills that request.

This separation preserves the architectural boundaries while allowing complex business operations to remain organized and maintainable.

---

[← When Orchestration Is Not Used](03-when-orchestration-is-not-used.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Common Architectural Mistakes →](05-common-failure-modes.md)