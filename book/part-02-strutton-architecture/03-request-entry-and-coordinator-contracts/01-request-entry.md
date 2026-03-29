# Request Entry

A request begins in the Presentation layer.

The API receives input from the outside world and translates that input into a form the system can understand. At this point, the system does not yet execute any business logic.

Instead, the request is transformed into a command or query.

This command or query represents an intention. It defines what the system should do, but not how it should do it.

This is an important distinction.

The Presentation layer does not know how the request will be handled. It only knows how to describe the request in a way that the system can process.

Once the command or query is created, it is sent into the Application layer.

From this point forward, execution is controlled by the architecture.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-coordinator-contracts.md)