# What Changes

While the architecture remains the same, its organization and enforcement evolve as systems scale.

Boundaries move.

In a clean monolith, boundaries exist within a single application. In a service-based system, boundaries become more explicit between modules. In microservices, boundaries become physical and enforced through deployment.

Communication changes.

Interaction that was once in-process becomes modular and eventually network-based. This introduces latency, failure scenarios, and the need for more careful coordination.

Deployment changes.

A single application becomes multiple deployable units. This increases flexibility but also increases operational complexity.

Ownership changes.

As systems grow, responsibility is often distributed across teams. This requires stronger boundaries and clearer contracts.

Operational complexity increases.

Monitoring, debugging, and maintaining the system becomes more difficult as it becomes more distributed.

These changes are not architectural.

They are consequences of scale.

---

[← Back](01-what-stays-the-same.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-this-distinction-matters.md)