# Chapter 5 — Orchestration

In the previous chapter, the Coordinator was introduced as the entry point for executing requests within the Application layer.

The next step is understanding how more complex workflows are handled.

Not all requests are equal. Some can be completed within a single transaction, while others require multiple steps that must be coordinated carefully.

This chapter introduces Orchestration.

## In this chapter, you will learn

- what Orchestration is and how it differs from the Coordinator  
- when Orchestration is required  
- when it should not be used  
- how Orchestration manages multi-step workflows  

This chapter focuses on coordinating execution when a request cannot be handled as a single, isolated operation.

---

[← Back](../04-coordinator-implementation/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-what-orchestration-is.md)