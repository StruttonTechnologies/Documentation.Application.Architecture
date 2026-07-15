# Request Entry

Every request begins in the Presentation layer.

The responsibility of the Presentation layer is to receive interaction from the outside world and describe that interaction in a form the architecture can understand. At this point, no business execution has begun.

Instead, the request is represented as a command or query.

A command or query describes **what** the caller wants the system to do without describing **how** that work will be performed. It represents intent rather than execution.

This distinction is fundamental.

The Presentation layer is responsible for describing the request, not executing it. It does not know how the request will be fulfilled, nor does it require knowledge of the architectural units responsible for execution.

Once the request has been described, it enters the Application layer through the architectural entry point defined by the Coordinator contracts.

From this point forward, execution is guided by the architecture rather than the Presentation layer.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Coordinator Contracts →](02-coordinator-contracts.md)