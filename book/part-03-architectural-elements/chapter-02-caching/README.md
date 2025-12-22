# Caching

## Overview

Caching is an architectural optimization used to improve performance and efficiency by **avoiding unnecessary recomputation or repeated access to slow resources**.

In this architecture, caching is treated as an **implementation concern**, not a behavioral one. It exists to enhance performance characteristics without altering application semantics or business rules.

Caching must never change what the system does—only how efficiently it does it.

---

## The Role of Caching in the Architecture

Caching exists to:

- Reduce latency for repeat access
- Decrease load on infrastructure resources
- Improve system responsiveness under scale
- Isolate performance optimizations from core behavior

It answers the question:

> “Can this result be reused safely?”

It does **not** answer:

> “What should the result be?”  
> “Is this behavior valid?”  
> “What decision should be made?”  

---

## Architectural Constraints

Caching is governed by strict architectural constraints to prevent correctness and consistency issues.

Caching must:

- Be transparent to business behavior
- Preserve correctness over performance
- Be safe to disable without altering outcomes
- Respect architectural boundaries

Caching must not:

- Encode business rules
- Drive control flow
- Replace persistence
- Mask data inconsistency or integrity problems

---

## Placement Within the Architecture

Caching may appear in multiple layers, but **for different reasons and with different responsibilities**.

- **Presentation Layer**  
  May cache presentation-specific artifacts (e.g., rendered views or responses)

- **Application Layer**  
  May cache use-case results where correctness is guaranteed and invalidation is explicit

- **Domain Layer**  
  Does not cache. Domain logic must remain deterministic and state-driven.

- **Infrastructure Layer**  
  May cache data access or integration results as a technical optimization

Caching must never leak across layers in a way that exposes implementation details.

---

## Relationship to Other Architectural Elements

Caching interacts with, but does not replace:

- Persistence
- Messaging
- Logging
- Configuration

Caching improves performance characteristics; it does not define system behavior.

---

## What You Will Learn in This Section

The pages in this section explain:

- Why caching is optional but powerful
- Where caching may safely exist
- How caching avoids polluting business logic
- Why correctness always outweighs performance

---

## Pages in This Section

- **[01 — Caching Boundaries](./01-caching-boundaries.md)**  
  What caching is allowed to do—and what it must never do

- **[02 — Caching Placement](./02-caching-placement.md)**  
  Where caching may exist without violating architectural intent

- **[03 — Cache Invalidation](./03-cache-invalidation.md)**  
  Why invalidation is an architectural concern, not an implementation detail

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-caching-boundaries.md">Next ▶</a>
</p>
