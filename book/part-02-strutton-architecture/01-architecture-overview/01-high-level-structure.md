# High-Level Structure

At a high level, the architecture is organized into distinct areas of responsibility. Each responsibility is represented by an architectural unit with a clearly defined purpose. Together, these architectural units form a system that is easier to understand, maintain, and evolve.

The architecture is organized primarily through layers for the system.

The **Presentation** layer is responsible for receiving requests and returning responses.

The **Application** layer coordinates execution. It contains the logic responsible for processing requests and determining how work should be performed.

The **Domain** layer represents the core business concepts, rules, and behaviors of the application.

The **Infrastructure** layer provides persistence and integrates with external systems and services.

In addition to these layers, the architecture contains supporting architectural units that fulfill responsibilities outside of the layered structure.

**Contracts** define the interactions exposed between architectural units while allowing implementation details to remain hidden behind assembly boundaries.

**ApplicationComposition** assembles the complete application. It gathers registrations from implementation assemblies and provides a single composition point for the application.

**Data Transfer Objects (DTOs)** define the shape of data exchanged between architectural units and external consumers. They represent information moving into and out of the system but do not participate in core business execution.

Together, these architectural units create a system where architectural integrity is reinforced through physical structure and controlled dependencies rather than relying solely on developer discipline and convention.

---

![Architecture Diagram](../../../assets/diagrams/ArchitectureDiagram.png)

---

[← Architecture Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Request Flow →](02-request-flow.md)