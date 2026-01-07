# Why Boundaries Exist

Architectural boundaries exist to control change.

They are not introduced for academic purity, stylistic preference, or visual symmetry.
They exist because uncontrolled knowledge flow makes systems fragile, difficult to
reason about, and expensive to evolve.

A boundary defines **where responsibility ends** and **where responsibility begins**.
Without boundaries, every part of a system becomes implicitly responsible for every
other part.

---

## Boundaries Are About Knowledge, Not Code

A boundary is not a physical construct.

It is not:
- a folder
- a namespace
- a project
- a deployment unit

Those are implementation tools.

A boundary exists wherever **knowledge is intentionally limited**.

When one part of a system does not know about the internal structure, behavior, or
dependencies of another part, a boundary exists between them.

Architecture is the deliberate placement of those boundaries.

---

## The Cost of Missing Boundaries

When boundaries are absent or poorly enforced, predictable failure modes appear:

- Controllers accumulate business logic
- Infrastructure details leak into application behavior
- Domain rules become coupled to frameworks
- Code reviews become subjective and inconsistent
- Refactoring one area causes ripple effects elsewhere

These outcomes are not caused by bad developers. They are caused by architectures that
rely on *discipline* instead of *structure*.

---

## Boundaries Enable Independent Change

A well-defined boundary allows one part of the system to change without forcing change
in another.

This independence is the primary value of architecture.

Boundaries allow:
- user interfaces to evolve independently of business rules
- application workflows to change without altering persistence mechanisms
- infrastructure technology to be replaced without rewriting core logic

Without boundaries, every change becomes a negotiation across the entire codebase.

---

## Boundaries Are Enforced, Not Remembered

Architectural rules that rely on memory, convention, or team discipline inevitably fail.

This architecture treats boundaries as **enforceable constraints**, not guidelines.

Enforcement is achieved through:
- dependency direction
- explicit contracts
- controlled composition
- restricted visibility

When a boundary is enforced structurally, violating it requires deliberate effort rather
than accidental convenience.

---

## Boundaries Precede Layers

Layers are a consequence of boundaries, not the other way around.

A layer exists because a boundary exists around a responsibility.

For example:
- the Presentation layer exists because interaction concerns are separated
- the Application layer exists because orchestration must be isolated
- the Domain layer exists because business rules must remain stable
- the Infrastructure layer exists because technical details must be contained

Understanding boundaries first makes layers intuitive rather than arbitrary.

---

## Boundaries as the Foundation of the Model

Every concept introduced later in this part depends on boundaries:

- Architectural Units exist to define what may cross boundaries
- Layers exist as bounded execution zones
- Runtime flow describes behavior moving through bounded structure

If boundaries are misunderstood, the rest of the architecture becomes easy to misuse.

For this reason, boundaries are introduced first and treated as foundational.

---

<p align="center">
  <a href="./README.md">◀ Chapter Overview</a>
  &nbsp;|&nbsp;
  <a href="./02-entering-vs-crossing.md">Entering vs Crossing ▶</a>
</p>
