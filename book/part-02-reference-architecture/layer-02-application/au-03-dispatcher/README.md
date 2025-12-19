# AU-03 — Dispatcher

## Overview

The Dispatcher Architectural Unit represents the **execution gateway** of the application.

It receives application intent, validates it, translates it into domain interaction, and routes execution to the appropriate path.

The Dispatcher does not define business rules.  
It enforces **how work flows through the system**.

---

## The Role of the Dispatcher

The Dispatcher is responsible for:

- Validating incoming DTOs
- Translating DTOs into domain entities and value objects
- Selecting the appropriate execution path
- Invoking repositories for simple operations
- Delegating complex workflows to orchestration
- Translating results back into DTOs

It is the **single touch point** through which application execution flows.

---

## Architectural Positioning

The Dispatcher sits:

- After contracts
- Before domain interaction
- Outside orchestration
- Above infrastructure

This positioning is intentional and structural.

---

## Topics in This AU

- **[01 — The Dispatcher as an Execution Gateway](01-execution-gateway.md)**

---

<p align="center">
  <a href="../au-02-dispatcher-contracts/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-execution-gateway.md">Next ▶</a>
</p>
