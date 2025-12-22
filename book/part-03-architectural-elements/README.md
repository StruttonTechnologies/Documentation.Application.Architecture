# Part 03 — Architectural Elements

## Purpose

This part of the book describes the **architectural elements** that support and shape the application architecture.

Architectural elements are **cross-cutting technical concerns** that are not owned by a single layer, but whose correct placement and usage are essential to maintaining architectural integrity.

This part does not describe *how* to implement these elements.  
It defines *what they are*, *why they exist*, and *how they relate to the architecture*.

---

## What This Part Covers

The sections in this part examine architectural elements such as:

- Logging
- Caching
- Messaging and events
- Configuration
- Validation

Each section explains:

- The architectural role of the element
- Where it is allowed to live
- Which layers may interact with it
- What responsibilities it must **not** take on

---

## What This Part Is Not

This part does **not**:

- Specify frameworks, libraries, or packages
- Provide code examples or configuration samples
- Act as an implementation guide
- Replace Core Capabilities documentation

Those concerns belong in separate documents and guides.

---

## Relationship to Other Parts

- **Foundations** define the principles that govern architectural decisions
- **Architecture Deep Dive** defines layers and Architectural Units
- **Architectural Elements** define shared technical concerns that operate *within* those boundaries

Together, these parts describe a complete architectural system.

---

## Sections in This Part

- **[Logging](./logging/README.md)**  
  How observability is achieved without violating architectural boundaries

- **[Caching](./caching/README.md)**  
  How performance optimization is introduced without polluting business logic

- **[Messaging & Events](./messaging/README.md)**  
  How asynchronous communication fits into the architecture without replacing boundaries

- **[Configuration](./configuration/README.md)**  
  How runtime behavior is configured without embedding decisions in code

- **[Validation](./validation/README.md)**  
  How correctness is enforced without duplicating domain rules

Some sections may be introduced incrementally as the architecture evolves.

---

<p align="center">
  <a href="../part-02-architecture-deep-dive/README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./logging/README.md">Next ▶</a>
</p>
