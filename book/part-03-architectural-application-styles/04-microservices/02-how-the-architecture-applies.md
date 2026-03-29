# How the Architecture Applies

The architecture does not change when moving to microservices.

Each service still contains its own internal structure.

- layers still exist  
- boundaries are still enforced  
- contracts still define interaction  
- DTOs and entities remain separated  

What changes is where those boundaries exist.

Instead of modules within a single application, each service becomes its own architectural unit.

Interaction between services occurs through external contracts rather than internal ones.

This introduces a new constraint.

Communication is no longer immediate. It is subject to network latency, partial failure, and consistency challenges.

Because of this, architectural discipline becomes more important, not less.

---

[← Back](01-what-microservices-are.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-what-you-gain.md)