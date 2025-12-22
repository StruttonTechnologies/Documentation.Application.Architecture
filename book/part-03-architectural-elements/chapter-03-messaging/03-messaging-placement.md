# Messaging Placement

## Responsibility

The responsibility of messaging placement is to ensure that **asynchronous communication supports the architecture without redefining it**.

Messaging infrastructure may span layers, but the *decision to communicate asynchronously* must originate from explicit application intent. Placement determines whether messaging remains a coordination mechanism or becomes an uncontrolled execution path.

---

## Why Placement Matters

Messaging introduces indirection and concurrency.

Without explicit placement rules, messaging can bypass architectural boundaries, distribute behavior across consumers, and make execution paths difficult to reason about. When this happens, the architecture becomes implicit rather than intentional.

Placement rules exist to ensure that:

- Application intent remains the source of behavior
- Responsibility is clearly owned
- Asynchronous execution remains traceable
- Architectural boundaries remain intact

---

## Placement by Layer

### Presentation Layer

The Presentation layer does not interact directly with messaging.

Presentation responsibilities end at expressing intent through application entry points. Introducing messaging here would allow asynchronous behavior to bypass application contracts and obscure execution paths.

Presentation remains synchronous and declarative.

---

### Application Layer

The Application layer owns **messaging intent**.

Responsibilities include:

- Deciding when a command should result in an event
- Determining whether work should proceed asynchronously
- Defining which outcomes are significant enough to publish

The Application layer may publish events or issue commands to messaging mechanisms, but it does not implement transport, delivery, or durability.

This preserves messaging as a coordination decision, not a technical shortcut.

---

### Domain Layer

The Domain layer does not interact with messaging infrastructure.

Domain logic may conceptually raise domain events to describe state transitions, but these events remain **in-memory and synchronous** until the Application layer decides how they are used.

This keeps the Domain independent of delivery concerns and preserves deterministic behavior.

---

### Infrastructure Layer

The Infrastructure layer implements **message transport and delivery**.

Responsibilities include:

- Message brokers or queues
- Delivery guarantees
- Retry and durability mechanisms
- Serialization and deserialization

Infrastructure does not decide *what* messages are sent or *when* they are published. It only ensures that messages requested by the Application layer are delivered reliably.

---

## Messaging Across Boundaries

Messaging must never be used to bypass architectural boundaries.

- Commands must still pass through application entry points
- Events must originate from completed application behavior
- Consumers must respect the same layer constraints as synchronous execution

Asynchronous does not mean boundary-free.

---

## Architectural Outcome

When messaging placement is respected:

- Execution intent remains explicit
- Asynchronous behavior remains understandable
- Responsibility remains centralized
- The system scales without becoming opaque

Messaging enhances the architecture—it does not redefine it.

---

<p align="center">
  <a href="./02-commands-vs-events.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../configuration/README.md">Next ▶</a>
</p>
