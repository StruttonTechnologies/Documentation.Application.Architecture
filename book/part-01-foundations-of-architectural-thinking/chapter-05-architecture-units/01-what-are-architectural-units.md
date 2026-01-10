# What Architectural Units Are

An architectural unit is a deliberate unit of responsibility that exists to make architectural intent explicit and enforceable. It is not defined by code size, runtime behavior, or deployment boundaries, but by the responsibility it owns and the role it plays within the architecture. Architectural units give architects a way to reason about systems at a level that aligns with design decisions rather than implementation detail.

Architectural units exist to make architecture tangible. They provide named, bounded elements that can be referenced, constrained, and composed without collapsing architectural thinking into individual classes or functions.

---

## Architectural Units Represent Ownership

Each architectural unit owns a clearly defined responsibility. That ownership is intentional and stable, even as implementation details change. The unit defines what it is accountable for and, just as importantly, what it is not accountable for. This clarity allows architects and teams to reason about change without repeatedly renegotiating boundaries.

Ownership at the unit level prevents responsibility from dissolving into shared assumptions or informal conventions. When responsibility is explicit, it can be defended and enforced.

---

## Architectural Units Operate Within Layers

Architectural units do not replace layers. They operate within them. A layer defines a zone of responsibility at the architectural level, while units define how that responsibility is packaged and addressed within that zone. This separation allows layers to remain conceptually stable while units evolve as the system grows.

Units give structure to layers without redefining them. They allow architects to express intent at a granularity that matches real systems without compromising the clarity of the layered model.

---

## Architectural Units Enable Intentional Interaction

Architectural units make interaction explicit. When units interact, those interactions can be reasoned about, constrained, and reviewed. This is essential in architectures that rely on closed layers, where interaction must occur through defined paths rather than convenience.

By naming and bounding interaction points, architectural units allow architects to control how responsibilities collaborate without allowing them to merge.

---

## Architectural Units Are Conceptual, Not Technical

Architectural units exist independently of how they are implemented. A unit may map to one or more projects, libraries, or services, but those mappings are expressions of the architecture, not its definition. Changing the physical structure of the code does not redefine the unit’s responsibility.

When architectural units are inferred from code rather than defined deliberately, architecture becomes reactive instead of intentional.

---

## Why This Definition Matters

Without architectural units, architecture is discussed in vague terms like “the application” or “the system.” Those abstractions are too coarse to enforce responsibility or constrain interaction meaningfully. Architectural units provide the precision needed to design, explain, and defend architecture at scale.

They are the bridge between conceptual architecture and real systems.

---

<p align="center">
  <a href="./README.md">◀ Chapter Overview</a>
  &nbsp;|&nbsp;
  <a href="./02-what-architectural-units-are-not.md">What Architectural Units Are Not ▶</a>
</p>
****