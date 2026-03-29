# Validation and Mapping

Validation and mapping occur within the Coordinator as part of request handling.

Validation ensures that incoming data is correct before execution begins. This prevents invalid requests from reaching deeper parts of the system and keeps execution focused on valid input.

Mapping prepares data for execution.

Requests enter the system as DTOs. These DTOs represent incoming data and are structured for interaction. Before execution begins, this data must be prepared so it can be used by the system.

This preparation happens in the Coordinator.

At this stage, the request is validated and shaped into a form suitable for execution. The details of how data transitions into domain representations are covered in the next section.

Keeping validation and mapping at this level ensures that deeper parts of the system receive only valid and properly prepared data.

---

[← Back](02-handlers-and-execution.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](04-dto-to-entity-transition.md)