# AU-01 — Frontend Architectural Units

## Overview

Frontend Architectural Units represent the **user-facing and client-facing surfaces** of the system.

They are the parts of the application that users and external actors interact with directly. Frontends render interfaces, collect input, and present outcomes, but they do not define application behavior or enforce business rules.

Frontends exist to provide experiences.  
They do not determine how the system works.

---

## Frontends in an API-Driven Architecture

This architecture is intentionally **API-driven**.

All frontends — regardless of technology — interact with the system exclusively through the API Delivery Architectural Unit. As a result, frontend technologies are interchangeable and do not shape application behavior.

A frontend may be:

- A web application
- A Blazor application
- A mobile client
- A desktop application
- An external system or integration

From an architectural perspective, all frontends are treated the same.

---

## What You Will Learn in This AU

The pages in this Architectural Unit explain the responsibilities that govern how frontends interact with the system and why those responsibilities exist.

Together, they describe how frontend flexibility is achieved without compromising architectural integrity.

Specifically, this section covers:

- **Client Independence**  
  Why no frontend technology is architecturally privileged

- **Execution Delegation**  
  Why frontends express intent but never execute application behavior

- **Boundary Enforcement**  
  How strict boundaries prevent frontend-driven coupling

- **Contract Stability**  
  Why frontends depend on explicit contracts rather than internal behavior

Each responsibility is discussed independently and builds toward a complete understanding of the frontend’s architectural role.

---

## How to Read This AU

You may read the pages in this AU sequentially or jump directly to a specific responsibility using the links below.

Each page is self-contained and focuses on **architectural intent**, not implementation detail.

---

## Topics in This AU

- [01 — Client Independence](01-client-independence.md)
- [02 — Execution Delegation](02-execution-delegation.md)
- [03 — Boundary Enforcement](03-boundary-enforcement.md)
- [04 — Contract Stability](04-contract-stability.md)

---

<p align="center">
  <a href="../README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./01-client-independence.md">Next ▶</a>
</p>
