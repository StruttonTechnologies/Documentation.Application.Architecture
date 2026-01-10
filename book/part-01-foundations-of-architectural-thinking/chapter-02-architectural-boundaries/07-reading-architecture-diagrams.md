# Reading Architecture Diagrams

Architecture diagrams are not decorations.

They are compressed representations of decisions, constraints, and intent. When read correctly, a diagram communicates what is allowed, what is forbidden, and where responsibility lives—often more clearly than prose.

This section explains how to read architecture diagrams as **expressions of structure**, not illustrations of implementation.

---

## Diagrams Communicate Constraints, Not Behavior

An architecture diagram does not show how the system runs.

It shows:
- Boundaries
- Direction of dependency
- Separation of responsibility
- Points of interaction

If you approach a diagram looking for execution flow, you will misread it. Architecture diagrams describe **structure**, not runtime behavior.

---

## Boxes Represent Responsibility, Not Code Size

A common mistake is to interpret the size or placement of boxes as a measure of importance or complexity.

In this book:
- A box represents a **unit of responsibility**
- It may contain many projects—or very few
- Its size does not imply scope, effort, or value

Boxes exist to answer one question:
> *Who owns this responsibility?*

---

## Lines Represent Allowed Knowledge Flow

Lines and arrows are the most important elements in an architecture diagram.

They indicate:
- Which direction dependencies are allowed
- Where boundaries are crossed
- Which interactions are intentional

If a line does not exist, the interaction is not allowed.

If a dependency exists in code but not in the diagram, the architecture has been violated.

---

## Direction Matters More Than Connection

Two components being connected is less important than **how** they are connected.

Direction answers:
- Who depends on whom
- Who absorbs change
- Who remains stable

Bidirectional arrows are rare in well-architected systems. They usually indicate unclear responsibility or missing boundaries.

---

## Diagrams Are Prescriptive, Not Descriptive

The diagram in this book is not a snapshot of current implementation.

It is a **prescription**.

Implementation is expected to conform to the diagram—not the other way around. When the two disagree, the diagram is the source of truth.

If the diagram becomes outdated, it must be corrected *before* implementation drifts further.

---

## Why This Matters Before the Final Architecture

Later in this book, the full architecture diagram will be introduced.

By the time you reach it, you should already know how to:
- Identify boundaries
- Interpret direction
- Understand responsibility
- Spot violations instinctively

This section ensures the diagram communicates clearly—without requiring explanation on every page.

---

<p align="center">
  <a href="./06-cqrs-as-a-thinking-model.md">◀ CQRS as a Thinking Model</a>
  &nbsp;|&nbsp;
  <a href="../part-01-foundations-of-architectural-thinking/README.md">Part I Overview ▶</a>
</p>
