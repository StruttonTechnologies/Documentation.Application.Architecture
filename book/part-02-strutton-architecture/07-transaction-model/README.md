# Chapter 7 — Transaction Model

In the previous chapter, repository contracts and persistence were introduced as controlled mechanisms for interacting with data.

The next step is understanding how changes to data are managed.

Not all operations follow the same pattern. Some can be completed in a single transaction, while others require multiple coordinated steps.

This chapter defines the transaction model used in this architecture.

## In this chapter, you will learn

- what a transaction represents in the system  
- how single-transaction requests are handled  
- how multi-step workflows are coordinated  
- how to determine which approach to use  

This chapter focuses on how data changes are controlled and applied within the architecture.

---

[← Back](../06-repository-and-persistence/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-what-a-transaction-is.md)