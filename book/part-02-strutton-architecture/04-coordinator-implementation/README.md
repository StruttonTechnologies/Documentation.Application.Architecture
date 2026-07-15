# Chapter 4 — Coordinator Implementation

The previous chapter introduced Coordinator contracts and established how requests enter the Application layer through a single, controlled architectural entry point.

Once a request has entered the architecture, responsibility shifts from interaction to execution.

This chapter introduces the Coordinator implementation, the architectural unit responsible for coordinating request execution. It explains how requests begin their execution, how responsibilities are delegated within the Application layer, and where the transition from interaction models to domain execution occurs.

## In this chapter, you will learn

- the responsibility of the Coordinator
- how requests begin execution within the Application layer
- where validation and transformation occur
- where interaction models transition into domain entities
- how the Coordinator delegates work while preserving architectural boundaries

By the end of this chapter, you will understand why the Coordinator is responsible for coordinating execution rather than performing every aspect of the request itself.

---

[← Request Entry and Coordinator Contracts](../03-request-entry-and-coordinator-contracts/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Role of the Coordinator →](01-role-of-the-coordinator.md)