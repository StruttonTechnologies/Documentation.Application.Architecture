# How Orchestration Works

When a request requires Orchestration, the Coordinator delegates execution.

Instead of handling all logic directly, the handler calls into the Orchestration layer through a contract. This maintains separation between coordination and execution.

The Orchestration layer then manages the workflow.

It determines the sequence of operations, invokes the necessary components, and ensures that each step is executed correctly.

This may involve:

- calling repositories multiple times  
- managing intermediate results  
- coordinating commits  

Each step is performed in a controlled manner.

The Coordinator initiates the process, but Orchestration manages how the work is carried out across multiple steps.

This keeps responsibilities clear.

---

[← Back](03-when-orchestration-is-not-used.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](05-common-failure-modes.md)