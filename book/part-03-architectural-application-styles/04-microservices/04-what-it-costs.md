# What It Costs

Microservices replace some forms of internal complexity with distributed complexity.

Communication now occurs across networks. Requests experience latency. Services may be unavailable independently. A workflow can succeed in one service and fail in another. Operations that were once locally transactional may require coordination across separate transaction boundaries.

Operational responsibility also increases.

Each service must be deployed, observed, secured, configured, supported, and recovered. Debugging requires tracing behavior across process and service boundaries. Testing must account for unavailable dependencies, delayed communication, incompatible contracts, and partial failure.

Data becomes more difficult to coordinate.

Clear ownership is necessary, but independently owned data introduces consistency and reporting challenges. Sharing a database may reduce short-term effort while quietly recreating the coupling the service boundaries were intended to prevent.

Organizational costs increase as well.

Teams must maintain contracts, coordinate changes, and accept responsibility for operating the services they own.

These costs are not arguments against microservices.

They are the price of independent deployment and distributed ownership.

Microservices are appropriate only when the benefits of that independence justify the permanent complexity the system and organization must carry.

---

[← What You Gain](03-what-you-gain.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Changes and What Stays the Same →](../05-what-changes-and-what-stays-the-same/README.md)
