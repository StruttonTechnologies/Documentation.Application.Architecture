# AU-02 — API Delivery Architectural Unit

## Overview

The API Delivery Architectural Unit represents the **primary entry point** into the application.

It is responsible for receiving requests from external clients, exposing application capabilities through explicit contracts, and delivering responses back to those clients.

In this architecture, the API exists to **accept intent and deliver outcomes**.  
It does not define application behavior or business rules.

---

## The API in an API-Driven Architecture

This architecture is intentionally **API-driven**.

All external interaction with the system — whether from a user interface, a mobile client, or an external integration — flows through the API Delivery Architectural Unit.

As a result:

- All clients interact with the system in the same way
- Application behavior is centralized and consistent
- Frontend technologies remain interchangeable
- Entry-point policy is enforced uniformly

The API defines *how the outside world interacts with the application*, not *how the application works internally*.

---

## What You Will Learn in This AU

The pages in this Architectural Unit explain the responsibilities that govern how the API exposes and protects application behavior.

Together, they describe how the API Delivery AU enables flexibility at the edges while preserving architectural integrity at the core.

Specifically, this section covers:

- **Single Entry Point**  
  Why all external interaction is funneled through the API

- **Execution Delegation**  
  Why the API delegates all behavior to the Application layer

- **Boundary Enforcement**  
  How the API protects internal layers from external coupling

- **Contract Stability**  
  Why explicit, stable contracts are critical to client interaction

Each topic is discussed independently and builds toward a complete understanding of the API’s architectural role.

---

## How to Read This AU

You may read the pages in this AU sequentially or jump directly to a specific topic using the links below.

Each page is self-contained and focuses on **architectural intent**, not implementation detail.

---

## Topics in This AU

- [01 — Single Entry Point](01-single-entry-point.md)
- [02 — Execution Delegation](02-execution-delegation.md)
- [03 — Boundary Enforcement](03-boundary-enforcement.md)
- [04 — Contract Stability](04-contract-stability.md)

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-single-entry-point.md">Next ▶</a>
</p>
