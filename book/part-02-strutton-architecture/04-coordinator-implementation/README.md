# Chapter 4 — Coordinator Implementation

In the previous chapter, requests were introduced as commands and queries that enter the system through Coordinator contracts.

The next step is understanding how those requests are executed.

This chapter focuses on the Coordinator implementation, where requests are processed and translated into actions within the system.

## In this chapter, you will learn

- the role of the Coordinator in handling requests  
- how handlers execute commands and queries  
- how validation and mapping are applied  
- where the transition from DTOs to entities occurs  

This chapter focuses on execution at the entry point of the application layer. Later chapters will explore how more complex workflows and persistence are handled.

---

[← Back](../03-request-entry-and-coordinator-contracts/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-role-of-the-coordinator.md)