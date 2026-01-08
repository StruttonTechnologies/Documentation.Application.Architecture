# Dependency Direction vs. Call Direction

A frequent source of architectural confusion is the assumption that dependency direction
follows call direction. In practice, these two concepts describe entirely different
relationships within a system.

Understanding the distinction between them is essential for reasoning about architecture,
enforcing boundaries, and evaluating design correctness.

---

## Call Direction Describes Runtime Behavior

Call direction describes what happens at runtime.

It answers questions such as:

- Which component invokes which operation
- Where execution begins and ends
- How control flows through the system

Call direction is dynamic and often varies based on configuration, input, or behavior.
It is an execution concern, not an architectural one.

---

## Dependency Direction Describes Knowledge

Dependency direction describes *who knows about whom* at design time.

It determines:

- Which types are visible
- Which contracts are referenced
- Which responsibilities are coupled

Dependency direction is static. It is established by project references and contracts,
not by runtime execution paths.

---

## Why the Distinction Matters

Confusing call direction with dependency direction leads to architectural mistakes.

A component may legitimately call into another component without depending on its
implementation. This is only possible when the dependency is inverted through an
abstraction or contract.

Conversely, a component may depend on another even if it never calls it directly.

Architecture is concerned with dependency direction, not invocation order.

---

## Inversion Enables Architectural Control

By inverting dependencies, high-level policies can remain independent of low-level
details.

In this architecture:

- Policies depend on contracts
- Implementations depend on those same contracts
- Call direction flows inward, while dependency direction points outward

This inversion allows execution flow without violating architectural boundaries.

---

## Architectural Review Implications

Understanding this distinction enables objective architectural review.

Rather than asking “who calls whom,” reviewers can ask:

- Which projects reference which contracts?
- Are dependencies flowing in the intended direction?
- Is any component gaining knowledge it should not have?

These questions are structural and verifiable.

---

## Preparing for Layering

Once dependency direction is clearly understood, architectural layers can be defined
without ambiguity.

The next subsection examines how dependency direction is enforced structurally and how
violations are prevented by design.

---

<p align="center">
  <a href="./subsection-01-why-dependency-direction-matters.md">◀ Previous Subsection</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./03-enforcing-dependency-direction.md">Next Subsection ▶</a>
</p>
