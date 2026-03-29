# How the Architecture Enforces Itself

This architecture enforces its structure through visibility and dependency control.

Each part of the system is only aware of what it is allowed to interact with.

The Presentation layer interacts with the system through contracts.

It does not have access to implementation assemblies. This prevents direct calls to execution logic and ensures that all requests follow the intended path.

The Application layer is divided into contracts and implementation.

Contracts define interaction. Implementation contains execution. This separation prevents external components from accessing internal behavior directly.

ApplicationComposition controls how the system is assembled.

It is the only place where implementation assemblies are referenced directly. This allows the system to be composed without exposing those implementations elsewhere.

DTOs and entities are separated.

DTOs are used for interaction. Entities are used for execution. This prevents external data structures from influencing internal behavior.

These rules are enforced by the structure of the system.

They do not rely on convention.

---

[← Back](01-why-enforcement-matters.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-what-this-prevents.md)