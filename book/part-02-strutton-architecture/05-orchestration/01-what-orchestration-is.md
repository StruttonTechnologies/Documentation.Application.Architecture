# What Orchestration Is

Orchestration is responsible for coordinating multi-step execution.

While the Coordinator handles individual requests, Orchestration manages workflows that involve multiple operations or transactions.

These workflows may require:

- multiple interactions with persistence  
- conditional execution paths  
- coordination between different parts of the system  

Orchestration does not define business rules.

It defines how work is organized and executed across multiple steps.

This distinction is important.

The Coordinator executes a request. Orchestration coordinates how that execution is carried out when it involves more than a single operation.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-when-orchestration-is-used.md)