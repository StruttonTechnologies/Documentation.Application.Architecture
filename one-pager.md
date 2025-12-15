# Core Capabilities Reference Architecture — Executive Summary

This document presents the reference architecture used by the **Core Capabilities** platform.
It defines the structural rules, boundaries, and execution model that all compliant applications
are expected to follow.

The architecture is designed for professional .NET systems that value:

- Explicit execution flow
- Enforced architectural boundaries
- Predictable composition and dependency direction
- Long-term maintainability across teams and projects

---

## Architectural Goals

The architecture exists to address the following systemic problems:

- Uncontrolled coupling between application layers
- Ambiguous ownership of responsibilities
- Hidden execution paths and implicit behavior
- Inconsistent onboarding and code review outcomes

---

## High-Level Model

At a high level, the system is organized into four primary layers:

- **Presentation** — Entry points and external interaction
- **Application** — Use case execution and orchestration
- **Domain** — Business rules and invariants
- **Infrastructure** — Technical implementations and external systems

Each layer communicates exclusively through explicit contracts.

(See: `diagrams/layer-dependencies.png`)

---

## Core Architectural Decisions

This architecture makes several non-negotiable decisions:

- Visibility is enforced through contracts, not convention
- Composition is centralized and explicit
- Dispatching and orchestration are separate concerns
- The API references a single composition surface
- Cross-layer communication is intentional and reviewable

These decisions are expanded upon throughout this book.

---

## How to Use This Book

This book explains **what the architecture is** and **why it exists**.

It does **not** explain:
- How to wire services in Program.cs
- How to use specific NuGet packages
- How to build an application step-by-step

Those concerns are intentionally addressed in companion documents.

---

<p align="center">
  <a href="index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="book/part-01-foundations/README.md">Begin Architecture ▶</a>
</p>
