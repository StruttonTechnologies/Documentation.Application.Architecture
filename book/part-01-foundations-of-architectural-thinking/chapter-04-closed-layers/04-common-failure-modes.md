# Common Failure Modes

Closed layers fail for the same reason most architectural constructs fail. The intent is sound, but enforcement erodes under pressure. These failure modes are rarely dramatic. They emerge gradually through reasonable decisions that accumulate until closure exists in name but not in behavior. This page exists to surface those patterns so they can be recognized and addressed early.

---

## Closure Becomes Conditional

One of the most common failure modes occurs when closure is treated as situational rather than absolute. Exceptions are introduced for convenience, urgency, or perceived low risk. Each exception feels justified on its own, but collectively they undermine the premise of closure.

This failure often appears as:
- special cases that bypass defined entry points
- rules that apply most of the time but not always
- debates about whether a violation is worth fixing
- architectural intent overridden by deadlines

Closure that only applies when it is convenient is not closure.

---

## Entry Points Multiply Without Intent

Closed layers rely on carefully designed entry points to coordinate interaction and protect responsibility. Failure occurs when new entry points are added reactively without reconsidering the layer’s role or the responsibilities it owns. Over time, the layer becomes accessible through many paths, each justified independently.

Common signals include:
- multiple parallel entry paths serving similar purposes
- entry points added to avoid refactoring existing ones
- unclear ownership of interaction logic
- difficulty explaining how the layer is meant to be used

When everything becomes an entry point, nothing is protected.

---

## Closure Is Delegated to Convention

Another failure mode arises when closure is documented but not enforced structurally. Teams are expected to “know better” and follow the rules voluntarily. This works until context is lost, teams change, or pressure increases.

This typically looks like:
- architectural rules written but not enforced
- violations addressed through review instead of structure
- reliance on shared understanding rather than constraints
- inconsistent adherence across teams

Architecture that depends on memory will not survive change.

---

## Closure Is Confused With Isolation

Closed layers fail when closure is mistaken for isolation. In an attempt to protect responsibility, layers are made difficult to access or understand, discouraging legitimate use. This creates workarounds rather than compliance.

Warning signs include:
- excessive indirection with unclear purpose
- duplication introduced to avoid interaction
- teams bypassing layers rather than engaging with them
- frustration replacing understanding

Closure should clarify interaction, not obstruct it.

---

## Enforcement Is Deferred Indefinitely

A final failure mode occurs when enforcement is acknowledged but postponed. Violations are tolerated with the intention of fixing them later. Over time, those violations become embedded, and enforcing closure becomes increasingly costly.

This pattern often includes:
- planned cleanups that never occur
- exceptions that become permanent
- selective enforcement based on urgency
- architecture that exists only in documentation

Architecture that relies on future discipline is fragile by design.

---

## Why These Failures Persist

Closed layers do not fail because they are too strict. They fail because enforcement is softened to accommodate short-term needs. Without consistent enforcement, closure loses its meaning and becomes indistinguishable from open layering.

Recognizing these failure modes is one of the architect’s primary responsibilities.

---

<p align="center">
  <a href="./03-why-use-closed-layers.md">◀ Why You Would Use Closed Layers</a>
  &nbsp;|&nbsp;
  <a href="../chapter-05-architecture-units/README.md">Architectural Units ▶</a>
</p>
