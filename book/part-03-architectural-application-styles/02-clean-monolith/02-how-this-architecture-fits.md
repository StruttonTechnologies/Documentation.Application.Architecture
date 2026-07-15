# How This Architecture Fits

The Strutton Technologies Application Architecture maps naturally to a clean monolith.

The complete execution model exists within one deployable application, but its responsibilities remain separated through the physical and conceptual structure established in Part 2.

The API exposes the application boundary.

Coordinator contracts define request entry. Coordinator implementation coordinates individual requests. Orchestration coordinates broader workflows when required. Repository contracts govern persistence interaction, and infrastructure fulfills persistence responsibilities.

ApplicationComposition assembles those responsibilities without exposing their implementations throughout the application.

DTOs remain interaction representations. Domain entities remain internal business representations. Transaction ownership remains with the architectural unit coordinating the work.

All of these responsibilities operate in-process, but they do not become architecturally indistinguishable.

The boundaries are enforced through contracts, assembly visibility, dependency direction, and controlled composition rather than through network separation.

This is how a single deployable application can remain architecturally closed and internally disciplined.

---

[← What a Clean Monolith Is](01-what-a-clean-monolith-is.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Why It Works →](03-why-it-works.md)
