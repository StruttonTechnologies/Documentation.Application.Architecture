# Chapter 6 — Boundary Space

In the previous chapters, layers were introduced to organize responsibility, boundaries were introduced to separate that responsibility, direction was introduced to control how dependencies flow, and contracts were introduced to define how interaction is allowed.

The next step is understanding where that interaction takes place.

Not all parts of a system serve the same purpose. Some areas are responsible for executing behavior, while others exist to handle interaction between different parts of the system or between the system and the outside world.

This chapter introduces the concept of boundary space.

## In this chapter, you will learn

- what boundary space is and how it differs from execution space  
- how interaction is separated from core system behavior  
- why this separation is important for maintaining structure  
- common ways boundary space breaks down in real systems  

This is not about specific technologies or entry points. It is about understanding how interaction is isolated from execution within a well-structured system.

---

[← Back](../05-contracts-and-interaction/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-what-boundary-space-is.md)