# What Architecture Is

Before we can talk about structure, boundaries, or enforcement, we need a clear and shared definition of **architecture** as it is used in this book.

This definition is intentionally narrow.

That is not a limitation—it is a safeguard.

---

## Architecture Is About System Shape

In this book, **software architecture** is concerned with the *shape of the system*.

That shape is defined by:
- How responsibilities are divided
- Where boundaries exist
- How those boundaries are crossed
- What is allowed to depend on what
- What knowledge is permitted to flow, and in which direction

Architecture answers questions like:
- *Where does this responsibility belong?*
- *What is allowed to know about what?*
- *What must never be coupled together?*
- *What decisions must be impossible to violate?*

If a decision does not affect the shape of the system, it is not architectural.

---

## Architecture Is a Set of Constraints

A common misconception is that architecture is about providing options.

In reality, architecture exists to **remove options**.

Good architecture:
- Reduces ambiguity
- Narrows decision space
- Makes incorrect designs hard or impossible
- Forces consistency through structure, not discipline

An architectural rule that can be ignored under pressure is not a rule—it is a preference.

This is why this book treats architecture as **structural and enforceable**, not advisory.

---

## Architecture Operates Above Implementation

Architecture does not describe *how* code is written.  
It describes *where* code belongs and *how* parts of the system are allowed to interact.

Architecture operates at a level where:
- Multiple implementations are possible
- Technologies can change
- Frameworks can be replaced
- Teams can evolve

If an architectural decision becomes invalid when a framework changes, it was likely an implementation decision disguised as architecture.

---

## Architecture Is About Responsibility, Not Mechanics

Architecture defines **who owns what**, and **who does not**.

It assigns responsibility to:
- Layers
- Boundaries
- Architectural units
- Contracts

It deliberately avoids:
- Method-level design
- Class structure
- Code patterns
- Performance optimizations

Those are engineering concerns. They matter—but they are downstream from architecture.

---

## Architecture Must Be Defensible

Every architectural decision must be defensible in terms of:
- Clarity
- Responsibility
- Separation
- Enforceability

“Because it’s simpler”  
“Because that’s how we usually do it”  
“Because the tooling allows it”  

These are not architectural justifications.

Architecture exists precisely to resist convenience when convenience erodes structure.

---

## Why This Definition Matters

If architecture is treated as:
- A set of diagrams
- A collection of best practices
- A reflection of current implementation

Then it cannot serve its purpose.

Architecture must be stable under change.  
It must remain valid as systems grow, teams expand, and pressure increases.

That stability comes from **clear boundaries and enforceable constraints**—not from convention.

---

<p align="center">
  <a href="./README.md">◀ Chapter Overview</a>
  &nbsp;|&nbsp;
  <a href="./02-what-architecture-is-not.md">What Architecture Is Not ▶</a>
</p>
