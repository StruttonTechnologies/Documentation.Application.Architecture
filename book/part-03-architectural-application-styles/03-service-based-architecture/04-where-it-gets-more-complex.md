# Where It Gets More Complex

Service-based architecture introduces stronger boundaries, but those boundaries require deliberate coordination.

The system must define who owns shared information, how modules communicate, and how behavior spanning multiple business areas is coordinated. Contracts become more significant because direct implementation access would undermine the module boundaries.

Data ownership also becomes more explicit.

Allowing every module to reach into the same persistence structures can create hidden coupling even when the code appears modular. Clear ownership is required so one module does not silently depend on another module's internal data model.

Cross-module workflows require care.

A business operation may involve several modules, but that does not justify dissolving their boundaries. The system must coordinate the workflow through explicit contracts while preserving the ownership of each participating responsibility.

Team and release coordination may also become more demanding, particularly when modules evolve at different rates.

These costs are lower than those of fully distributed microservices, but they are still real.

Service-based architecture provides value when stronger business separation solves an actual organizational or architectural problem. Introducing modules without clear responsibilities merely creates additional structure without meaningful ownership.

---

[← Why Modules Matter](03-why-modules-matter.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Microservices →](../04-microservices/README.md)
