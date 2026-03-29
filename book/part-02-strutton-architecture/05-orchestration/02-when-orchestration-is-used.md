# When Orchestration Is Used

Orchestration is used when a request requires multiple steps to complete.

This typically occurs when:

- more than one transaction is required  
- operations must occur in a specific sequence  
- decisions must be made between steps  
- multiple parts of the system must be coordinated  

In these scenarios, handling everything within a single handler would make the logic difficult to understand and maintain.

Orchestration provides structure.

It separates the coordination of work from the execution of individual steps, allowing each part of the system to remain focused on its responsibility.

---

[← Back](01-what-orchestration-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-when-orchestration-is-not-used.md)