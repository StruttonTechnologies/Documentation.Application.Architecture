# Layer 03 — Domain

## Overview

The Domain layer represents the **core business model** of the application.

It contains the concepts, rules, and structures that define *what the business is*, independent of how the application is delivered, orchestrated, or persisted.

In this architecture, the Domain is intentionally **simple, expressive, and isolated**.

---

## The Domain in This Architecture

The Domain layer exists to model business concepts, not application behavior.

It is composed exclusively of:

- **Entity models**  
  Objects with identity and lifecycle

- **Value objects**  
  Immutable objects that describe concepts or measurements

- **Enumerations**  
  Controlled sets of domain-specific values

These elements describe the business in its own language, without reference to infrastructure, persistence, or delivery concerns.

---

## What Does Not Belong in the Domain

In this architecture, the Domain layer deliberately does **not** contain:

- Repository interfaces
- Infrastructure abstractions
- Application orchestration
- Framework dependencies
- Technical concerns of any kind

All boundary-crossing interfaces live outside the Domain, in dedicated contract Architectural Units.

This choice preserves the Domain as a **pure representation of business intent**, not a coordination mechanism.

---

## Architectural Units in This Layer

The Domain layer contains the following Architectural Unit:

- **AU-01 — Domain Model Architectural Unit**  
  The authoritative definition of business entities, value objects, and enumerations

This AU is explored through its structural responsibilities rather than interaction patterns.

---

## What You Will Learn in This Layer

The pages in this layer explain:

- How business concepts are modeled
- Why the Domain remains free of interfaces and abstractions
- How purity enables long-term flexibility
- How other layers depend on the Domain without coupling it outward

This layer focuses on **expression and integrity**, not execution.

---

## How to Read This Layer

You may read this layer sequentially or use it as a reference when reasoning about business rules and model design.

All examples and explanations are architectural in nature and avoid implementation detail.

---

<p align="center">
  <a href="../layer-02-application/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./au-01-domain-model/README.md">Next ▶</a>
</p>
