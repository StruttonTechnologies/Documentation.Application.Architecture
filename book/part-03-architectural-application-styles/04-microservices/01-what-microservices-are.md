# What Microservices Are

Microservices are a way of organizing a system into independently deployed services.

Each service represents a distinct area of responsibility and operates as its own application. Services communicate with each other over a network rather than through direct in-process calls.

This is a change in deployment and communication, not in architecture.

The same principles still apply.

- responsibilities must be clearly defined  
- boundaries must be enforced  
- interaction must be controlled through contracts  

The difference is that these boundaries are now physical.

Instead of existing within a single application, they exist across independently deployed services.

This makes the separation stronger.

It also makes coordination more complex.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-how-the-architecture-applies.md)