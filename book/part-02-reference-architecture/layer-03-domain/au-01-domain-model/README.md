# AU-01 — Domain Model Architectural Unit

## Overview

The Domain Model Architectural Unit represents the **authoritative expression of business concepts** within the application.

It contains the models that define what the business *is*, independent of how the system is delivered, orchestrated, or persisted.

In this architecture, the Domain Model is intentionally **pure, expressive, and isolated**.

---

## The Role of the Domain Model

The Domain Model exists to describe business reality.

It defines:

- The entities the business cares about
- The values that describe those entities
- The controlled vocabularies used to reason about the domain

The Domain Model does **not** describe how data is stored, how use cases are executed, or how requests enter the system.

Its purpose is **expression**, not coordination.

---

## What Belongs in the Domain Model

The Domain Model AU contains only the following constructs:

- **Entities**  
  Objects with identity and lifecycle that represent core business concepts

- **Value Objects**  
  Immutable objects that describe attributes, measurements, or concepts

- **Enumerations**  
  Explicit sets of domain-specific values

Together, these constructs form the shared language of the business.

---

## What Does Not Belong in the Domain Model

In this architecture, the Domain Model deliberately excludes:

- Repository interfaces
- Infrastructure abstractions
- Application services
- Framework dependencies
- Technical concerns of any kind

All contracts used to cross architectural boundaries live outside the Domain, in dedicated contract Architectural Units.

This separation preserves the Domain as a **pure representation of business intent**.

---

## What You Will Learn in This AU

The pages in this Architectural Unit explain:

- How entities are modeled and protected
- Why value objects are immutable
- How invariants are expressed and preserved
- Why the Domain contains no interfaces
- How purity enables long-term architectural flexibility

Each topic focuses on **model integrity**, not interaction patterns.

---

## How to Read This AU

This AU may be read sequentially or used as a reference when reasoning about domain design.

Each page is self-contained and avoids implementation-specific guidance, focusing instead on architectural intent.

---

## Topics in This AU

- [01 — Entity Integrity](01-entity-integrity.md)  
  How entities preserve identity and enforce business invariants

- [02 — Value Object Immutability](02-value-object-immutability.md)  
  Why value objects are immutable and behavior-focused

- [03 — Explicit Invariants](03-explicit-invariants.md)  
  How business rules are enforced within the model

- [04 — Domain Purity](04-domain-purity.md)  
  Why the Domain contains no interfaces or technical abstractions


<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-entity-integrity.md">Next ▶</a>
</p>
