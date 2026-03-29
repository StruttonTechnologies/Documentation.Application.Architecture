# Chapter 9 — Presentation and Client Architecture

Up to this point, the focus has been on how the system is structured internally and how requests move through it.

The next step is understanding how the system is exposed and consumed.

In this architecture, the Presentation layer is not tied to a specific user interface. The API exists as the boundary of the system, while user interfaces remain clients of that boundary.

This chapter explains how presentation and client interaction are intentionally separated from application behavior.

## In this chapter, you will learn

- how the API acts as the system boundary  
- how user interfaces act as clients of the system  
- how multiple user experiences can be supported without duplicating behavior  
- why this separation improves flexibility and maintainability  

This chapter focuses on how the system is consumed, not how execution is performed internally.

---

[← Back](../08-dtos-entities-and-domain-visibility/05-common-failure-modes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-api-as-system-boundary.md)