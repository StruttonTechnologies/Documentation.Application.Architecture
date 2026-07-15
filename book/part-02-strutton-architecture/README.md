# Part 2 — Strutton Technologies Application Architecture

Part 1 introduced the foundational concepts of software architecture.

Layers, boundaries, dependency direction, and contracts established a conceptual model for organizing responsibilities and controlling interaction within a software system.

This part applies those concepts to a complete application architecture.

Rather than introducing new architectural principles, it demonstrates how those principles work together to create a cohesive, maintainable, and self-enforcing system.

Each chapter focuses on a specific architectural responsibility and the role it plays within the overall application.

## In this part, you will learn

- how the application is composed while controlling visibility
- how requests enter the system through architectural contracts
- how execution is coordinated through the Coordinator and Orchestration layers
- how persistence is abstracted through repository contracts
- how data moves through the system using DTOs and entities
- how the Presentation layer remains separate from application behavior
- how the architecture enforces itself through structure rather than convention

The goal is not simply to describe an application.

It is to demonstrate how architectural principles become an executable architectural model.

Throughout this part, every major responsibility is assigned a clear owner, every interaction follows defined architectural contracts, and every boundary exists to preserve the long-term integrity of the system.

By the end of this part, you will understand not only what the Strutton Technologies Application Architecture looks like, but why each responsibility exists and how those responsibilities work together to create a predictable, maintainable software system.

---

[← Part 1 Summary](../part-01-foundations-of-architecture/99-part-01-summary/README.md) |
[Table of Contents](../04-table-of-contents.md) |
[Architecture Overview →](01-architecture-overview/README.md)