# What ApplicationComposition Is

ApplicationComposition is responsible for assembling the application.

It provides a single composition point where the independently developed architectural units that make up the system are brought together to form a complete application.

Rather than requiring the application entry point to understand every implementation assembly, ApplicationComposition owns that responsibility. It gathers registrations from across the system and assembles them into a single, cohesive application.

This separates construction from execution.

The responsibility of building the application belongs to ApplicationComposition. The responsibility of executing the application belongs to the architectural units it assembles. By separating these concerns, the application entry point remains focused on starting the application rather than understanding how it is constructed.

ApplicationComposition is itself an architectural unit.

Unlike most architectural units, it is intentionally allowed to reference implementation assemblies because its responsibility is to construct the system rather than participate in its runtime behavior.

This distinction is fundamental to the architecture.

By isolating composition into a single controlled area, architectural boundaries remain intact while implementation details remain hidden from the rest of the application. The result is an architecture that reinforces its own structure instead of relying solely on developers to preserve it.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Distributed Registration →](02-distributed-registration.md)