# What It Costs

Microservices introduce significant complexity.

Communication is no longer in-process.

Every interaction between services involves network communication. This introduces latency, failure scenarios, and the need for retry and resilience strategies.

Consistency becomes more difficult.

Transactions cannot easily span multiple services. Coordinating changes across services requires careful design and often introduces eventual consistency.

Operational overhead increases.

Each service must be deployed, monitored, and maintained. This requires infrastructure, tooling, and operational maturity.

Debugging becomes harder.

Tracing behavior across multiple services is more complex than within a single application.

These costs are often underestimated.

Microservices are not a simplification.

They are a tradeoff.

---

[← Back](03-what-you-gain.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../05-what-changes-and-what-stays-the-same/README.md)