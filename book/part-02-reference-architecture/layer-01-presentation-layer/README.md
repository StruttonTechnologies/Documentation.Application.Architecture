# Presentation Layer

## Overview

The Presentation layer represents the **entry boundary** of the application.

It contains the components responsible for receiving input from users and external systems, translating that input into application intent, and returning results in an appropriate format.

The Presentation layer does not execute business logic or define application behavior. It serves as a controlled gateway into the system.

In the reference architecture, this layer demonstrates how foundational principles—such as boundary enforcement, dependency direction, and explicit contracts—are applied concretely at the system boundary.

---

## Presentation in This Architecture

In this architecture, the Presentation layer is intentionally **thin and disciplined**.

It does not:

- Contain business rules
- Execute use cases directly
- Access persistence mechanisms
- Coordinate workflows

Instead, the Presentation layer exists to:

- Accept requests
- Translate input into application intent
- Delegate execution inward through explicit contracts
- Return results to the caller

All meaningful behavior occurs beyond this boundary.

---

## Composition and Startup

The Presentation layer is also responsible for **application composition**.

Composition is the process of assembling implementations from multiple layers into a runnable application. This includes wiring contracts to concrete implementations and producing the final application object graph.

By locating composition in the Presentation layer, the architecture ensures that:

- Application and Domain layers remain implementation-agnostic
- Infrastructure details do not leak inward
- Dependency direction is enforced structurally
- Startup behavior remains explicit and predictable

Composition is a startup concern, not application behavior.

---

## Responsibility Boundaries

The Presentation layer is responsible for:

- Accepting input from users and external systems
- Translating input into application intent
- Delegating execution to the Application layer
- Performing application composition and startup wiring
- Returning results to callers

It is **not responsible** for:

- Business rules
- Use-case orchestration
- Validation beyond input shape
- Authorization decisions
- Persistence or transactional behavior

These boundaries are enforced through contracts and project references.

---

## Architectural Units in This Layer

The Presentation layer is divided into Architectural Units (AUs), each addressing a distinct responsibility at the system boundary.

### Architectural Units

- **[AU-01 — Frontend](./au-01-frontend/README.md)**  
  Defines how user-facing clients interact with the system

- **[AU-02 — API](./au-02-api/README.md)**  
  Defines the single, controlled entry point into the application

- **[AU-03 — Composition & Dependency Injection](./au-03-composition/README.md)**  
  Defines how implementations are wired together at startup

Each AU begins with a high-level overview, followed by focused responsibility pages.

---

## Dependency Direction

All dependencies originating from the Presentation layer point **inward**.

- Presentation depends on:
  - Application contracts
  - Infrastructure contracts
  - Composition mechanisms

- Presentation does not depend on:
  - Application implementations
  - Domain logic
  - Infrastructure details

This ensures that the Presentation layer remains a boundary, not a source of behavior.

---

## How to Read This Layer

You may read the Architectural Units sequentially or jump directly to a specific concern.

If you are new to the architecture, begin with **Frontend** to understand client responsibilities, then proceed to **API**, and finally **Composition & Dependency Injection** to see how the system is assembled.

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./au-01-frontend/README.md">Next ▶</a>
</p>
