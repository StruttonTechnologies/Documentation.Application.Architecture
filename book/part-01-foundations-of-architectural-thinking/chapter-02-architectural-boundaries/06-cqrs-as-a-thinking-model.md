# CQRS as a Thinking Model

CQRS—Command Query Responsibility Segregation—is often introduced as a technical pattern. In this book, it is treated differently.

Here, CQRS is a **thinking model**.

It is a way for architects to reason clearly about intent, responsibility, and system interaction long before any implementation decisions are made.

---

## Commands and Queries Represent Different Kinds of Intent

At the architectural level, there are only two kinds of interactions with a system:

- **Commands**: requests to change state
- **Queries**: requests to observe state

These two intents are fundamentally different.

Commands:
- Express intent to modify the system
- Carry business meaning
- Must be validated, constrained, and controlled

Queries:
- Express intent to read information
- Do not change system state
- Should be predictable and side-effect free

Treating these as the same kind of operation blurs responsibility and increases risk.

---

## CQRS Clarifies Responsibility

When commands and queries are separated conceptually:
- It becomes clear where state changes are allowed
- Validation logic has a defined home
- Side effects are easier to reason about
- Read concerns stop leaking into write logic

CQRS does not require separate databases, services, or infrastructure.  
It requires **clarity of intent**.

---

## CQRS Is About Direction, Not Technology

CQRS introduces direction into system interaction.

Commands flow *into* the system.  
Queries flow *out* of the system.

That directionality aligns naturally with:
- Boundaries
- Closed layers
- Controlled entry points

When direction is unclear, responsibilities overlap. CQRS restores clarity by making intent explicit.

---

## CQRS Prevents Accidental State Change

One of the most common architectural failures is accidental state mutation.

This often happens when:
- Reads and writes are mixed
- Convenience methods do too much
- Side effects are hidden in query paths

By separating commands and queries conceptually, architects reduce the surface area where state can change.

That reduction is architectural, not technical.

---

## CQRS Without Ceremony

CQRS is frequently over-implemented.

This book does **not** assume:
- Separate read and write models
- Messaging infrastructure
- Event sourcing
- Distributed systems

CQRS here is about **separation of responsibility**, not ceremony.

The goal is to make intent obvious and violations detectable.

---

## Why CQRS Belongs in Foundations

CQRS reinforces every concept introduced so far:
- Boundaries
- Direction
- Responsibility
- Enforcement

By treating CQRS as a thinking model rather than a pattern, architects gain a tool for evaluating structure before implementation begins.

It prepares the ground for later chapters where these ideas become concrete.

---

<p align="center">
  <a href="./05-closed-layers.md">◀ Closed Layers</a>
  &nbsp;|&nbsp;
  <a href="./07-reading-architecture-diagrams.md">Reading Architecture Diagrams ▶</a>
</p>
