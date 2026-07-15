# Chapter 5 — Orchestration

The previous chapter introduced the Coordinator and explained how individual requests are coordinated within the Application layer.

Not all requests, however, can be completed through a single request execution.

Some business operations require multiple steps, multiple transactions, or coordination across several architectural responsibilities while still presenting a single logical operation to the caller.

This chapter introduces Orchestration.

Orchestration extends the architecture beyond the execution of an individual request by coordinating more complex workflows while preserving the same architectural boundaries established throughout the system.

## In this chapter, you will learn

- the responsibility of the Orchestration layer
- how Orchestration differs from the Coordinator
- when orchestration is appropriate
- when it should be avoided
- how complex workflows are coordinated while preserving architectural boundaries

By the end of this chapter, you will understand why coordination of a single request and orchestration of a broader workflow are separate architectural responsibilities.

---

[← Coordinator Implementation](../04-coordinator-implementation/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Is Orchestration? →](01-what-orchestration-is.md)