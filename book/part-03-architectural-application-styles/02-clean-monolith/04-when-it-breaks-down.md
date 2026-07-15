# When It Breaks Down

A monolith does not fail merely because it is deployed as one unit.

It fails architecturally when its internal structure is no longer preserved.

When responsibilities spread, boundaries are bypassed, shared areas become dumping grounds, and dependencies form without control, the application gradually becomes an unstructured monolith. The problem is not the deployment model. The problem is architectural erosion.

A clean monolith may also reach legitimate limits.

Different parts of the system may require independent release schedules. Specific capabilities may need to scale separately. Teams may require stronger ownership boundaries. Availability or regulatory requirements may demand greater isolation.

These pressures do not automatically require microservices.

They indicate that the current organization and deployment model should be reevaluated.

The architecture itself does not need to be discarded. Its responsibilities and boundaries need to be reorganized into a style capable of satisfying the new constraints.

The transition should occur because the existing style no longer meets demonstrated needs, not because distribution is assumed to be the natural destination of every successful system.

---

[← Why It Works](03-why-it-works.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Service-Based Architecture →](../03-service-based-architecture/README.md)
