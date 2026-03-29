# How It Differs from a Clean Monolith

A clean monolith and a service-based architecture share the same underlying principles.

The difference is in how those principles are organized.

In a clean monolith, the system is structured as a single set of layers with enforced boundaries.

In a service-based architecture, those layers exist within each module.

Each module contains its own internal structure, while still participating in the overall system.

This creates a higher level of separation.

Instead of enforcing boundaries across the entire system, boundaries are enforced both within modules and between modules.

The system remains a single deployment.

However, the internal organization becomes more explicit and more structured.

---

[← Back](01-what-service-based-architecture-is.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-modules-matter.md)