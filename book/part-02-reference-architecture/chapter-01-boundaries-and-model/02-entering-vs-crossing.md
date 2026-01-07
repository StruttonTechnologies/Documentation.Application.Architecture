# Entering a Layer vs Crossing a Boundary

One of the most common sources of architectural confusion is the failure to distinguish
between **entering a layer** and **crossing a boundary**.

These two actions are not the same, and treating them as equivalent leads directly to
over-abstraction, duplicated models, and inconsistent enforcement.

This architecture makes the distinction explicit.

---

## What It Means to Enter a Layer

Entering a layer means that **execution moves into a different responsibility zone**.

When execution enters a layer:
- control flow continues inward
- behavior is invoked directly
- no data is exchanged across responsibility boundaries
- no contract is required

Entering a layer is a matter of execution, not communication.

For example:
- Application code enters the Domain layer to evaluate business rules
- Domain code enters infrastructure implementations through inversion
- Execution moves deeper into policy, not outward into details

Because responsibility remains aligned, no boundary is crossed.

---

## What It Means to Cross a Boundary

Crossing a boundary means that **data or intent moves between responsibility zones**.

When a boundary is crossed:
- one part of the system communicates intent to another
- knowledge must be restricted
- structure must be protected
- an explicit contract is required

Crossing a boundary is not about execution flow—it is about **controlled exchange**.

For example:
- Presentation communicating intent to the Application layer
- Application exposing outcomes to external consumers
- Composition wiring capabilities without exposing implementations

Boundaries are crossed only through Architectural Units.

---

## Why This Distinction Matters

Failing to distinguish entering from crossing leads to predictable mistakes:

- Interfaces are created where none are needed
- DTOs are duplicated unnecessarily
- Domain models are flattened to satisfy external concerns
- Controllers take on orchestration responsibilities
- Enforcement relies on discipline instead of structure

These outcomes are often rationalized as “clean architecture,” but they stem from a
misapplied mental model.

---

## The Domain Layer as an Example

The Domain layer illustrates this distinction clearly.

Application code **enters** the Domain layer to execute business logic. It does not
*cross* into it.

Because no exchange occurs:
- domain entities do not require interfaces
- domain models do not need DTOs
- domain behavior remains concrete and expressive

The Domain layer is entered, not negotiated with.

This is intentional.

---

## Where Contracts Are Required

Contracts exist **only where boundaries are crossed**, not where layers are entered.

In this architecture:
- DTOs represent boundary-safe data
- Dispatcher contracts represent boundary-safe intent
- Composition contracts define allowable wiring

Contracts are not added to “improve abstraction.”  
They exist to **enforce separation where responsibility changes**.

---

## A Rule You Can Apply Consistently

The distinction can be summarized as a simple rule:

> **If execution moves inward to fulfill responsibility, a layer is entered.  
> If data or intent moves sideways across responsibility, a boundary is crossed.**

Layers are entered.  
Boundaries are crossed.

If a boundary is crossed without a contract, the architecture is already compromised.

---

## How This Rule Guides the Rest of the Architecture

This distinction explains why:
- Architectural Units exist
- DTOs are boundary representations
- Service composition is centralized
- Layers remain concrete internally
- Runtime flow can be traced reliably

It is the conceptual thread that ties structure, enforcement, and execution together.

---

<p align="center">
  <a href="./01-why-boundaries-exist.md">◀ Why Boundaries Exist</a>
  &nbsp;|&nbsp;
  <a href="./03-enforcement-over-guidelines.md">Enforcement Over Guidelines ▶</a>
</p>
