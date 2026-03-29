# How This Architecture Fits

The architecture described in Part 2 maps directly to a clean monolith.

All layers exist within the same application, but they are separated by structure rather than by deployment.

- The Presentation layer exposes the system boundary  
- The Application layer coordinates execution  
- The Domain defines behavior  
- The Infrastructure handles persistence  

Contracts enforce interaction between these areas.

ApplicationComposition controls how the system is assembled and prevents direct access to implementation details.

Even though everything runs as a single application, boundaries are still real.

They are enforced through visibility and dependency control, not through physical separation.

This is what makes the monolith clean.

---

[← Back](01-what-a-clean-monolith-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-it-works.md)