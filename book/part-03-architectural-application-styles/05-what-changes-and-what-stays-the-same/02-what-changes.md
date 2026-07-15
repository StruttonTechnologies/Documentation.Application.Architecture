# What Changes

Although the architectural principles remain consistent, the mechanisms used to represent and enforce them change as the application style evolves.

Boundaries become more explicit.

In a clean monolith, boundaries are primarily enforced within one application. In a service-based system, business modules strengthen those boundaries. In microservices, selected boundaries also become process, network, and deployment boundaries.

Communication changes.

In-process interaction may become cross-module communication and eventually distributed communication. Latency, availability, compatibility, and partial failure become part of architectural decision-making.

Transaction scope changes.

A local application may coordinate work within one transaction boundary. Distributed services own separate transactions, requiring business workflows to account for independent completion and failure.

Deployment and operation change.

One release unit becomes several. Independent deployment provides flexibility while increasing the need for observation, coordination, support, and recovery.

Ownership becomes more explicit.

As responsibilities are divided among modules, services, and teams, contracts and data authority require greater discipline.

These are meaningful changes.

They are changes in organization, communication, deployment, and operation—not replacements for the underlying architecture.

---

[← What Stays the Same](01-what-stays-the-same.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Why This Distinction Matters →](03-why-this-distinction-matters.md)
