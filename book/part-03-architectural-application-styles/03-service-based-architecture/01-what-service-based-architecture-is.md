# What Service-Based Architecture Is

Service-based architecture organizes a system into a small number of business-aligned services or modules with clearly defined responsibilities.

These units are more explicit than the internal layers of a clean monolith, but they do not necessarily require the fine-grained distribution associated with microservices.

A service-based system may still be deployed as one application, as several larger deployable services, or through a combination of both. The defining characteristic is not the number of deployments.

It is the strength of the business boundaries.

Each service or module owns a cohesive area of behavior, its internal implementation, and the contracts through which other parts of the system interact with it.

The architecture established in Part 2 remains applicable within each unit.

Responsibilities remain explicit. Contracts regulate interaction. Internal implementation remains hidden. Dependency direction remains controlled. The architecture continues to enforce the intended boundaries.

Service-based architecture therefore strengthens organization without assuming that every responsibility requires an independent distributed service.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[How It Differs from a Clean Monolith →](02-how-it-differs-from-a-clean-monolith.md)
