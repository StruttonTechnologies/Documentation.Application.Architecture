# What Architecture Is Not

Clarifying what architecture *is* only works if we are equally clear about what it is **not**.

Much of the confusion architects experience—especially early in their careers—comes from architecture being overloaded with responsibilities it was never meant to carry. When everything is architecture, architecture loses its authority.

This section draws firm boundaries around the role of architecture by explicitly stating what falls **outside** of it.

---

## Architecture Is Not Implementation

Architecture does not describe how code is written.

It does not define:
- Classes
- Methods
- Design patterns
- Algorithms
- Performance optimizations
- Coding conventions

Those are implementation concerns. They matter, but they live *within* the structure defined by architecture.

If an architectural discussion devolves into how code should be written, the boundary between architecture and engineering has already been crossed.

---

## Architecture Is Not Framework Selection

Choosing a framework, library, or platform is not architecture.

Frameworks:
- Change frequently
- Impose their own constraints
- Come with assumptions that may or may not align with the system’s needs

Architecture must **outlive** frameworks.

If an architectural decision only makes sense for a specific framework, then the framework—not the architecture—is in control.

This book treats frameworks as *guests* inside the architecture, not as structural authorities.

---

## Architecture Is Not a Coding Style Guide

Architecture does not define:
- Naming conventions
- Folder layouts
- Formatting rules
- Code aesthetics

Those concerns are important for consistency and maintainability, but they do not shape the system itself.

A beautifully formatted system with unclear boundaries is still architecturally weak.

---

## Architecture Is Not a Collection of Best Practices

Best practices are contextual.  
Architecture must be **intentional**.

Following industry norms without understanding why they exist leads to:
- Inherited assumptions
- Cargo-cult designs
- Architectural drift disguised as pragmatism

This book does not aim to replicate common industry patterns. It aims to define a coherent, enforceable architectural model that serves a specific purpose.

---

## Architecture Is Not Flexible by Default

Flexibility is often praised as a virtue in architecture.

Unconstrained flexibility, however, is indistinguishable from ambiguity.

Architecture exists to:
- Make some choices impossible
- Prevent entire classes of mistakes
- Remove decision-making from places where it does not belong

Flexibility that undermines clarity is not a benefit—it is a liability.

---

## Why These Distinctions Matter

When architecture is expected to solve everything, it solves nothing.

By clearly defining what architecture does *not* do, we:
- Preserve architectural authority
- Protect boundaries from erosion
- Allow engineering to operate effectively within constraints
- Reduce conflict between roles and responsibilities

Architecture is most effective when it is precise, limited, and enforced.

---

<p align="center">
  <a href="./01-what-is-architecture.md">◀ What Architecture Is</a>
  &nbsp;|&nbsp;
  <a href="./03-why-architecture-exists.md">Why Architecture Exists ▶</a>
</p>
