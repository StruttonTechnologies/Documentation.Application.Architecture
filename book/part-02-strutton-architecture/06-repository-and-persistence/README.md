# Chapter 6 — Repository and Persistence

In the previous chapter, Orchestration was introduced as the mechanism for coordinating multi-step workflows.

The next step is understanding how the system interacts with persistence.

Data access is a critical part of any system, but it must be handled in a way that preserves the architecture.

This chapter introduces repository and persistence patterns used in this architecture.

## In this chapter, you will learn

- how repository contracts define data access  
- how persistence is abstracted from execution  
- how commits and transaction boundaries are controlled  
- how these elements work together within the architecture  

This chapter focuses on how data is accessed and modified without exposing implementation details or breaking architectural boundaries.

---

[← Back](../05-orchestration/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-repository-contracts.md)