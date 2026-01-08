# Chapter 02 — Architectural Units

This chapter introduces **Architectural Units (AUs)**.

Architectural Units are structural constructs that exist to **enforce architectural
boundaries**. They define what is allowed to cross boundaries, how composition is
controlled, and how responsibilities remain isolated over time.

Unlike execution layers, Architectural Units do not define where behavior runs.
They define **how interaction is constrained**.

---

## Why Architectural Units Exist

Boundaries define *where separation is required*.  
Architectural Units define *how that separation is enforced*.

Without Architectural Units, boundaries exist only in diagrams and documentation.
With Architectural Units, boundaries are expressed structurally and enforced by the
shape of the system.

Architectural Units make architectural intent explicit and enforceable.

---

## Architectural Units Are Not Layers

Architectural Units are often confused with layers. This architecture treats them as
distinct concepts.

- **Layers** define execution responsibility.
- **Architectural Units** define structural constraints.

Architectural Units:
- do not participate in runtime execution
- do not own business behavior
- do not define workflows
- do not replace layers

They exist to support layers, not compete with them.

---

## What Architectural Units Do

Architectural Units are responsible for:

- defining boundary-safe contracts
- limiting visibility and dependency direction
- centralizing composition policy
- separating structure from execution
- preventing accidental coupling

If something is allowed to cross a boundary, it does so through an Architectural Unit.

---

## Where Architectural Units May Exist

Architectural Units are flexible by design.

They may:
- exist **between layers** to define boundary contracts
- exist **independently** to define shared structure or composition
- exist **within a layer** to enforce internal separation

What matters is not *where* an AU lives, but *what responsibility it enforces*.

---

## Types of Architectural Units in This Architecture

This reference architecture includes several categories of Architectural Units.

Each category is described in detail in the sections that follow.

- **Application DTOs**  
  Boundary-safe representations used to exchange data without exposing internal models.

- **Dispatcher Contracts**  
  Explicit definitions of application intent that govern how requests enter
