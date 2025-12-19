# AU-01 — Application DTOs

## Overview

The Application DTOs Architectural Unit defines the **data contracts used to interact with the application**.

DTOs represent intent and outcome, not business state. They provide a stable, application-owned representation that is shared across entry points while protecting the domain from external concerns.

In this architecture, Application DTOs are **immutable records**.

---

## The Role of Application DTOs

Application DTOs exist to:

- Express application intent and results explicitly
- Decouple clients from internal models
- Provide a shared language across entry points
- Protect the domain from representation concerns
- Ensure requests and responses cannot be modified once created

DTOs shape communication, not behavior.

---

## Immutability of Application DTOs

Application DTOs are designed to be **immutable**.

Once created, a DTO represents a fixed expression of intent or result. It cannot be altered during execution. Any change in meaning requires the creation of a new instance.

Immutability ensures that:

- Intent cannot be mutated mid-execution
- Validation results remain trustworthy
- Execution flow is predictable and auditable
- DTOs are safe to pass across layers and boundaries

DTO immutability supports architectural correctness, not domain modeling.

---

## What Belongs in This AU

This Architectural Unit contains:

- Command DTOs
- Query DTOs
- Result / response DTOs

DTOs contain structure and meaning, but no business rules.

---

## What Does Not Belong Here

Application DTOs deliberately exclude:

- Domain entities or value objects
- Business invariants
- Persistence concerns
- Framework-specific behavior

They are contracts, not models.

---

## What You Will Learn in This AU

The pages in this AU explain:

- Who owns DTOs and why
- How DTOs form a translation boundary
- Why DTO immutability is required
- Why DTO stability is critical to architectural evolution

---

## Topics in This AU

- [01 — Contract Ownership](01-contract-ownership.md)
- [02 — Boundary Translation](02-boundary-translation.md)
- [03 — Stability Over Time](03-stability-over-time.md)

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-contract-ownership.md">Next ▶</a>
</p>
