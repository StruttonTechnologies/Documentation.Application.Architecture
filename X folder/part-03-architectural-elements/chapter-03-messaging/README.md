# Messaging & Events

## Overview

Messaging and events provide a mechanism for **asynchronous communication** within and across system boundaries.

In this architecture, messaging is used to **decouple execution timing**, not to replace architectural boundaries or obscure application intent. Events describe *what has already occurred*; messages coordinate *when work should occur*.

Messaging exists to support scale and resilience, not to redefine behavior.

---

## The Role of Messaging in the Architecture

Messaging exists to:

- Decouple producers from consumers
- Enable asynchronous processing
- Support eventual consistency where appropriate
- Improve system resilience under load or failure

It answers the question:

> “How can work proceed without requiring immediate coordination?”

It does **not** answer:

> “What behavior is allowed?”  
> “What business rule applies?”  
> “What decision should be made?”  

---

## Architectural Constraints

Messaging is governed by strict constraints to prevent erosion of architectural clarity.

Messaging must:

- Preserve explicit application intent
- Respect layer boundaries
- Remain observable and traceable
- Be optional to core correctness

Messaging must not:

- Replace application orchestration
- Encode business rules
- Hide execution paths
- Bypass architectural entry points

If messaging becomes required to understand system behavior, the boundary has been violated.

---

## Commands vs Events

This architecture distinguishes clearly between **commands** and **events**.

- **Commands**  
  Express intent to perform work. Commands are requests and may be rejected.

- **Events**  
  Describe something that has already happened. Events are facts and cannot be refused.

Confusing commands and events leads to implicit behavior and unclear responsibility.

---

## Placement Within the Architecture

Messaging may exist in multiple layers, but **responsibility differs by layer**.

- **Application Layer**  
  Owns the decision to emit commands or publish events

- **Infrastructure Layer**  
  Implements message transport, delivery, and durability

- **Domain Layer**  
  May raise domain events conceptually, but does not manage messaging infrastructure

- **Presentation Layer**  
  Does not interact directly with messaging mechanisms

---

## Relationship to Other Architectural Elements

Messaging interacts with:

- Logging (for observability)
- Configuration (for routing and delivery)
- Caching (for eventual consistency considerations)

Messaging complements synchronous execution; it does not replace it.

---

## What You Will Learn in This Section

The pages in this section explain:

- Why messaging is optional but powerful
- How commands and events differ architecturally
- Where messaging belongs—and where it does not
- How asynchronous behavior remains explicit

---

## Pages in This Section

- **[01 — Messaging Boundaries](./01-messaging-boundaries.md)**  
  What messaging is allowed to do—and what it must never do

- **[02 — Commands vs Events](./02-commands-vs-events.md)**  
  How intent and fact are kept distinct

- **[03 — Messaging Placement](./03-messaging-placement.md)**  
  Where messaging infrastructure fits without violating boundaries

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-messaging-boundaries.md">Next ▶</a>
</p>
