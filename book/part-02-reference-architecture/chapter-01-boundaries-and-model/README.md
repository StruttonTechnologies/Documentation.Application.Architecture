# Chapter 01 — Boundaries and Architectural Model

This chapter establishes the architectural model used throughout Part II.

Its purpose is not to describe specific layers, contracts, or runtime behavior in detail,
but to define the **rules of the system** and the **mental model** required to understand
everything that follows.

Boundaries are the foundation of this architecture. Without understanding what a boundary
is, why it exists, and how it is enforced, the remaining chapters cannot be interpreted
correctly.

---

## Why Boundaries Matter

Architectural boundaries exist to control change.

They determine:
- which parts of the system may know about each other
- where responsibilities begin and end
- how change is contained rather than propagated

In this architecture, boundaries are **not advisory**. They are enforced through structure.
Violating a boundary is not a matter of discipline or convention—it is made structurally
difficult or impossible.

This approach prioritizes **enforceability over intention**.

---

## Entering a Layer vs Crossing a Boundary

A critical distinction in this architecture is the difference between *entering* a layer
and *crossing* a boundary.

- **Entering a layer** means execution moves into a new responsibility zone.
- **Crossing a boundary** means data or intent moves between responsibility zones.

Layers are entered during execution. Boundaries are crossed only through explicit
Architectural Units.

This distinction explains why some elements require contracts and others do not.

For example:
- Application code may *enter* the Domain layer without using DTOs or interfaces.
- Presentation code may not *cross* into the Application layer without an explicit
  contract defining what is allowed to pass.

This rule is foundational and applies throughout the architecture.

---

## Architectural Units as Boundary Mechanisms

Architectural Units (AUs) exist to define what is allowed to cross boundaries.

They are not execution layers and do not own application behavior. Instead, they serve as
structural constructs that enforce separation, stability, and clarity.

Architectural Units may:
- exist independently of execution layers
- exist between layers
- exist within a layer to enforce internal separation

If something is allowed to cross a boundary, it does so through an Architectural Unit.

---

## Layers as Execution Zones

Layers define where behavior executes.

Each layer represents a distinct responsibility and enforces strict dependency direction.
Layers are entered during runtime and contain execution components that participate in
application behavior.

Layers do not communicate freely with one another. Any movement of data or intent across
layer boundaries must respect the architectural rules defined in this chapter.

The specific responsibilities of each layer are described in later chapters.

---

## Runtime Flow Is Not Structure

Runtime flow describes how behavior moves through the system over time.

It is not a layer, and it is not an Architectural Unit.

Understanding runtime flow requires first understanding:
- where boundaries exist
- how layers are entered
- what is allowed to cross between them

For this reason, runtime flow is described only after the structural model has been
established.

---

## How to Read the Diagrams

This book uses diagrams to describe both structure and behavior.

- **Structural diagrams** illustrate dependency direction and visibility.
  Arrows represent *knowledge and reference*, not runtime flow.
- **Flow diagrams** illustrate execution or data movement over time.

These diagram types serve different purposes and must not be interpreted interchangeably.

Understanding which type of diagram is being presented is essential for correct
interpretation.

---

## How This Chapter Fits into Part II

This chapter defines the rules that govern the rest of Part II.

- Chapter 02 describes **Architectural Units** that implement boundary enforcement.
- Chapter 03 describes **execution layers** and their responsibilities.
- Chapter 04 describes **runtime flow** within the bounded structure.

This chapter should be read carefully and referenced often. It provides the context
required to evaluate architectural decisions consistently and objectively.

---

<p align="center">
  <a href="../README.md">◀ Back to Part II</a>
  &nbsp;|&nbsp;
  <a href="../chapter-02-architectural-units/README.md">Architectural Units ▶</a>
</p>
