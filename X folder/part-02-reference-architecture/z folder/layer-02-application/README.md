# Layer 02 — Application

## Overview

The Application layer represents the **coordination and execution boundary** of the system.

It is responsible for translating external intent into domain interaction, coordinating workflows, and enforcing architectural direction. It does not define business meaning, nor does it implement technical concerns.

In this architecture, the Application layer is where **decisions are made**, not where rules are invented or data is stored.

---

## The Role of the Application Layer

The Application layer sits between **Presentation** and **Domain**.

Its responsibilities include:

- Accepting intent expressed through application contracts
- Validating requests at the application boundary
- Translating DTOs into domain concepts
- Deciding execution paths
- Coordinating workflows when necessary
- Returning results in a stable, client-facing form

The Application layer owns **how work is done**, not **what the business is**.

---

## Architectural Units in This Layer

The Application layer is composed of the following Architectural Units:

- **[AU-01 — Application DTOs](./au-01-application-dtos/README.md)**  
  Application-facing data contracts shared across entry points

- **[AU-02 — Dispatcher.Contracts](./au-02-dispatcher-contracts/README.md)**  
  Explicit command and query contracts that define application intent

- **[AU-03 — Dispatcher](./au-03-dispatcher/README.md)**  
  The execution gateway that validates, translates, and routes intent

- **[AU-04 — Orchestration.Contracts](./au-04-orchestration-contracts/README.md)**  
  Contracts that define multi-step workflows

- **[AU-05 — Orchestration](./au-05-orchestration/README.md)**  
  Workflow implementations operating on domain entities

Each AU is intentionally narrow and focused, enforcing architectural boundaries through structure rather than convention.

---

## What You Will Learn in This Layer

In this layer, you will learn:

- Why application contracts are distinct from domain models
- How handlers act as the system’s execution gateway
- Why orchestration is optional rather than mandatory
- How workflows are coordinated without bloating handlers
- How direction of dependency is preserved structurally

This layer defines **how the application behaves**, not how it is presented or persisted.

---

## How to Read This Layer

This layer may be read sequentially or referenced by Architectural Unit.

Each AU begins with a high-level overview and is followed by focused responsibility pages explaining architectural intent and tradeoffs.

---

<p align="center">
  <a href="../layer-03-domain/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./au-01-application-dtos/README.md">Next ▶</a>
</p>
