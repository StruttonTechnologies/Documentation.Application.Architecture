# Part II — Reference Architecture

This part defines the reference architecture used for applications built within the
Application Architecture described in this book.

Where Part I established foundational principles and constraints, this part applies
those principles to a concrete architectural model. It describes how the system is
structured, how responsibilities are divided, and how architectural rules are enforced
through explicit boundaries and composition.

This reference architecture is not an independent design. It is the direct consequence
of the principles defined in Part I.

---

## Purpose of This Part

The purpose of this part is to answer the following questions:

- How is the system structurally organized?
- Where does application behavior execute?
- What is allowed to cross architectural boundaries?
- How are responsibilities separated and enforced?
- How does the system behave at runtime?

By the end of this part, readers should have a clear mental model of the system’s
structure, execution responsibilities, and runtime flow.

---

## Architectural Model Overview

The reference architecture is based on a layered execution model consisting of:

- **Presentation Layer**
- **Application Layer**
- **Domain Layer**
- **Infrastructure Layer**

Layers define where behavior executes and enforce dependency direction.  
Each layer is composed of execution components that participate in runtime flow. Layers
are entered during execution and do not exchange data directly with one another without
crossing an explicit boundary.

In addition to layers, the architecture makes use of Architectural Units (AUs) to define
structural, contractual, and compositional concerns that do not themselves execute
application behavior.

---

## Boundaries, Architectural Units, and Runtime Flow

This part is organized into chapters, each focusing on a distinct architectural concern:

- **Boundaries and Architectural Model**  
  Defines what architectural boundaries are, why they exist, how they are enforced,
  and how to interpret the diagrams and structure used throughout this part.

- **Architectural Units (AUs)**  
  Structural constructs that define what may cross boundaries, how composition is
  enforced, and how responsibilities are separated. AUs may exist independently,
  between layers, or within a layer.

- **Execution Layers**  
  Behavioral zones where application logic executes. Layers contain execution
  components and are governed by strict dependency and visibility rules.

- **Runtime Flow**  
  A narrative description of how requests, commands, and queries move through the
  system over time. Runtime flow is not a layer or an AU, but an explanation of
  behavior in motion.

Together, these chapters form a complete and enforceable architectural model.

---

## Key Architectural Rules

The reference architecture adheres to the following rules:

- Dependencies flow inward toward stable policy
- Architectural boundaries are explicit and enforced
- Boundary crossing requires a defined Architectural Unit
- Composition is centralized and policy-driven
- Execution flow is intentional and traceable
- Infrastructure details are isolated from application behavior

These rules apply consistently across all chapters in this part.

---

## What This Part Covers

This part introduces the reference architecture chapter by chapter, describing:

- The purpose and responsibility of each architectural construct
- What it is allowed to depend on
- What it is not allowed to contain
- How boundaries are enforced structurally
- Common failure modes and architectural anti-patterns

Later parts of this book build upon this structure when discussing execution patterns,
platform concerns, and system evolution.

---

## Reading Guidance

This part should be read sequentially.

Each chapter builds on the previous ones and assumes familiarity with the foundational
principles described in Part I. Understanding the distinction between boundaries,
Architectural Units, execution layers, and runtime flow is essential for interpreting
the architecture that follows.

---

<p align="center">
  <a href="../part-01-foundations/README.md">◀ Previous Part</a>
  &nbsp;|&nbsp;
  <a href="../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./chapter-01-boundaries-and-model/README.md">Begin Part II ▶</a>
</p>
