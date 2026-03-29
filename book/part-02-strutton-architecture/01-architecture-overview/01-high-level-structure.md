# High-Level Structure

The architecture is organized into layers, contracts, and composition.



At a high level, the system is divided into distinct areas of responsibility.

The Presentation layer is responsible for receiving input and returning results.

The Application layer coordinates execution. It contains the logic that processes requests and determines how work should be performed.

The Domain represents the core business concepts and rules.

The Infrastructure layer handles persistence and external concerns such as data access.

In addition to these layers, there are supporting elements that exist outside of the layered structure.

Contracts define how interaction is allowed to occur between different parts of the system. They control visibility and prevent direct access to implementation details.

ApplicationComposition assembles the system. It collects registrations from each implementation assembly and exposes a single entry point for the application to use.

DTOs define the shape of data as it moves into and out of the system. They are used for interaction but do not participate in core execution.

These elements work together to form a system where structure is enforced through dependency control rather than convention.

---

![Architecture Diagram](../../../assets/diagrams/ArchitectureDiagram.png/)
---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-request-flow.md)