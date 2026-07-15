# Architecture vs Deployment

Architecture and deployment are related, but they are not the same thing.

Architecture defines the structure of a system. It assigns responsibilities, establishes boundaries, controls dependencies, and governs interaction.

Deployment defines how that system is packaged, released, and operated.

A monolith is not automatically an architecture.

A microservice is not automatically an architecture.

They are application and deployment styles that describe how parts of a system are organized and run. The quality of the architecture depends on the structure that exists within and between those deployable units.

The same architectural principles can be applied within a single deployable application, across several independently organized modules, or among many distributed services.

Confusing architecture with deployment leads to poor decisions.

A team may distribute a poorly structured system expecting deployment boundaries to solve unclear responsibilities or uncontrolled dependencies. Distribution does not correct those problems. It makes them more expensive to observe, coordinate, and change.

Architecture defines the rules of the system.

Deployment determines where and how those rules operate.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Scaling Really Means →](02-what-scaling-really-means.md)
