# Part II — Reference Architecture

This part defines the reference architecture used for applications built within the
Application Architecture described in this book.

Where Part I established foundational principles and constraints, this part applies
those principles to a concrete structural model. It describes the layers of the system,
their responsibilities, and the rules that govern how they interact.

---

## Purpose of This Part

The purpose of this part is to answer the following questions:

- How is the system structurally organized?
- What responsibilities belong to each layer?
- How do layers interact without violating architectural constraints?
- Where do architectural concerns such as composition and dispatching reside?

By the end of this part, readers should have a clear mental model of the system’s
structure and execution flow.

---

## Architectural Model Overview

The reference architecture is organized into a layered model consisting of:

- **Presentation Layer**
- **Application Layer**
- **Domain Layer**
- **Infrastructure Layer**

Each layer has a clearly defined responsibility and communicates with other layers
only through explicit, enforced boundaries.

The layered model is not an implementation convenience—it is a structural expression
of the architectural principles established in Part I.

---

## Key Architectural Rules

The reference architecture adheres to the following rules:

- Dependencies flow inward toward stable policy
- Visibility is constrained by contracts
- Composition is centralized
- Execution flow is explicit and traceable
- Infrastructure details are isolated from application logic

These rules are applied consistently across all layers.

---

## What This Part Covers

This part introduces each layer in turn, describing:

- Its purpose and responsibility
- What it is allowed to depend on
- What it is not allowed to contain
- Common failure modes and anti-patterns

Later parts of this book build upon this structure when discussing architectural
elements and platform capabilities.

---

## Reading Guidance

This part should be read sequentially. Each section builds on the previous one and
assumes familiarity with the foundational principles described earlier.

---

<p align="center">
  <a href="../part-01-foundations/README.md">◀ Previous Part</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./section-01-presentation-layer/README.md">Begin Part II ▶</a>
</p>
