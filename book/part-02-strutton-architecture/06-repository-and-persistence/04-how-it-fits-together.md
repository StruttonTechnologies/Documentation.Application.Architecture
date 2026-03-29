# How It Fits Together

Repository contracts and persistence abstraction work together to control data access.

The Coordinator or Orchestration layer interacts with repository contracts to perform data operations. These operations are executed by the persistence layer, which remains hidden behind the contracts.

Changes are not finalized until a commit occurs.

This ensures that the system maintains consistency and that operations are performed within defined transaction boundaries.

The flow remains consistent with the overall architecture.

- Requests enter through contracts  
- Execution occurs within the Application layer  
- Data access is performed through repository contracts  
- Persistence is handled by the Infrastructure layer  
- Changes are committed in a controlled manner  

Each step follows the architectural rules.

This keeps the system predictable and easier to maintain.

---

[← Back](03-commit-and-transaction-boundaries.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](05-common-failure-modes.md)