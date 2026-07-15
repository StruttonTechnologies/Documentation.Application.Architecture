# What Microservices Are

Microservices are independently deployable services organized around clearly defined business responsibilities.

Each service owns a cohesive capability, its internal behavior, and the data required to fulfill that responsibility. Other services interact with it only through explicitly defined contracts.

Independent deployment is a defining characteristic.

A service can be released, operated, and scaled without requiring the entire system to be deployed as one unit. This independence creates flexibility, but it also turns many internal interactions into distributed communication.

Microservices do not eliminate the need for internal architecture.

Each service still requires clear responsibilities, layers, boundaries, dependency direction, contracts, composition, execution flow, and persistence ownership. A service without internal structure is simply a small unstructured application.

The system also requires architecture between services.

Service boundaries must reflect meaningful ownership. Contracts must remain stable. Data must have clear authority. Cross-service behavior must acknowledge latency, partial failure, and independent change.

Microservices are therefore not architecture by themselves.

They are a distributed style in which architectural boundaries also become deployment boundaries.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[How the Architecture Applies →](02-how-the-architecture-applies.md)
