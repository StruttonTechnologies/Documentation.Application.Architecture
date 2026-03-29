# Chapter 3 — Request Entry and Coordinator Contracts

In the previous chapter, ApplicationComposition was introduced as the mechanism used to assemble the system and control visibility.

The next step is understanding how a request enters the system.

A request must be able to reach execution logic, but it must do so without exposing implementation details or allowing architectural boundaries to be bypassed.

This chapter introduces how requests are handled through Coordinator contracts.

## In this chapter, you will learn

- how requests enter the system through the Presentation layer  
- how Coordinator contracts define the entry point into execution  
- how visibility is controlled to prevent direct access to handlers  
- why this approach enforces architectural boundaries  

This chapter focuses on how interaction begins. The next chapter will explore how execution is handled once the request has entered the system.

---

[← Back](../02-application-composition/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-request-entry.md)