# How the Architecture Applies

The Strutton Technologies Application Architecture applies within each microservice.

A service can expose its own API boundary, accept requests through contracts, coordinate execution, orchestrate workflows, isolate persistence, protect its domain model, and assemble its internal implementation through controlled composition.

The same responsibility-driven architecture therefore exists inside every service.

What changes is the interaction between services.

Calls that were previously in-process now cross a network boundary. Contracts become externally significant. Failures may occur independently. Information may arrive late, more than once, or not at all. Transaction boundaries can no longer be assumed to span the complete business operation.

These changes require stronger ownership rather than weaker boundaries.

Each service must own its behavior and data. Other services request capabilities through contracts rather than accessing internal implementation or persistence directly. Cross-service workflows coordinate independent responsibilities without pretending they share one local execution context.

The architecture remains the same in principle.

Distribution changes the mechanisms, costs, and failure conditions through which those principles are realized.

---

[← What Microservices Are](01-what-microservices-are.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What You Gain →](03-what-you-gain.md)
