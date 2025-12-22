# Commands vs Events

## Responsibility

The responsibility of distinguishing commands from events is to ensure that **intent and fact are never conflated**.

Commands express a request for work to be performed.  
Events describe something that has already occurred.

This distinction preserves clarity, responsibility, and correctness—especially in asynchronous systems.

---

## Why the Distinction Matters

When commands and events are treated interchangeably, system behavior becomes ambiguous.

Without a clear distinction:

- Responsibility for outcomes becomes unclear
- Rejection and failure semantics are confused
- Behavior shifts from intentional to emergent

The architecture requires that intent and fact remain **separate concepts**.

---

## Commands

A **command** represents intent.

Commands are:

- Requests to perform work
- Directed at a specific capability
- Allowed to fail or be rejected
- Evaluated against rules and constraints

Architecturally, commands answer the question:

> “Should this work be performed?”

Commands originate from explicit application intent and are handled by application logic.

---

## Events

An **event** represents fact.

Events are:

- Statements about something that has already happened
- Immutable and non-rejectable
- Observed, not evaluated
- Free of conditional logic

Architecturally, events answer the question:

> “What has occurred?”

Events do not request behavior—they inform interested parties of outcomes.

---

## Queries and Events

Queries are intentionally excluded from this discussion.

Queries are **synchronous requests for information** and do not participate in asynchronous messaging or event publication. They retrieve current state; they do not describe intent and they do not describe outcomes.

Queries must never:

- Emit events
- Trigger asynchronous processing
- Encode side effects

This separation preserves the integrity of both CQRS and messaging concerns.

---

## Key Differences

| Aspect | Command | Event |
|------|---------|-------|
| Meaning | Intent | Fact |
| Timing | Before execution | After execution |
| Rejectable | Yes | No |
| Direction | Directed | Broadcast |
| Responsibility | Application | Observers |

Confusing these roles leads to unclear behavior and fragile systems.

---

## Architectural Usage Rules

- Commands must always originate from explicit application intent
- Events may only be emitted after a meaningful state change
- Commands must never be treated as facts
- Events must never request work
- Queries must never emit events

If an operation needs approval or validation, it is a command.  
If an operation has already occurred, it is an event.

---

## Relationship to Other Architectural Elements

The command/event distinction reinforces:

- **Dispatcher.Contracts**  
  Commands and queries define application intent

- **Orchestration**  
  Coordinates execution before events are emitted

- **Logging**  
  Observes both intent and outcomes without influencing them

- **Caching**  
  Must never assume commands have occurred until events confirm them

---

## Consequences of Confusion

When commands and events are confused:

- Systems become difficult to reason about
- Failures propagate unpredictably
- Debugging requires tracing implicit side effects
- Behavior becomes timing-dependent

Clear separation preserves architectural integrity under scale.

---

<p align="center">
  <a href="./01-messaging-boundaries.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-messaging-placement.md">Next ▶</a>
</p>
