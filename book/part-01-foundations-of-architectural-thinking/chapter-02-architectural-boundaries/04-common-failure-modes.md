# Common Failure Modes

Architectural boundaries rarely fail all at once.

They fail through a series of small, reasonable decisions that slowly erode separation, responsibility, and clarity. This section highlights the most common ways boundaries degrade in real systems—not to assign blame, but to make failure recognizable before it becomes permanent.

---

## Boundaries Reduced to Convention

One of the earliest failure modes is when boundaries exist only as guidance.

This usually sounds like:
- “We’re not supposed to reference that directly”
- “Try to go through the proper path”
- “Architecturally, this should be separate”

When enforcement is replaced with expectation, boundaries become optional. Optional boundaries are crossed under pressure—and once crossed, they stop being taken seriously.

---

## Interfaces Without Separation

Interfaces are introduced, but:
- They live alongside implementations
- Implementations are still directly accessible
- “Temporary” shortcuts bypass the interface

This creates the appearance of a boundary without the protection of one.

When an implementation is reachable, it *will* be depended on—regardless of intent.

---

## Knowledge Leakage Disguised as Convenience

Another common failure mode occurs when knowledge crosses a boundary “just to make things easier.”

Examples include:
- Exposing internal models for reuse
- Sharing configuration or utilities across boundaries
- Allowing downstream code to reason about upstream internals

Each instance feels harmless. Collectively, they erase the boundary.

Boundaries do not fail because of one bad decision—they fail because of many small ones.

---

## Responsibility Becomes Shared

When boundaries weaken, responsibility blurs.

Suddenly:
- Multiple areas feel entitled to change the same behavior
- Fixes span several parts of the system
- Ownership becomes unclear

At this point, architectural discussions shift from structure to coordination—which is a sign the boundary has already failed.

---

## “We’ll Fix It Later”

Perhaps the most dangerous failure mode is deferral.

Statements like:
- “We’ll clean this up later”
- “This is temporary”
- “We just need to get past this deadline”

are rarely followed by corrective action.

Temporary boundary violations have a habit of becoming permanent—especially once other code begins to rely on them.

---

## Why Architects Must Recognize These Patterns

These failure modes are common because they feel reasonable in isolation.

The architect’s responsibility is not to prevent change, but to prevent **unintentional structural change**. Recognizing these patterns early allows boundaries to be reinforced before erosion becomes systemic.

Boundaries do not protect themselves.  
They require attention, clarity, and enforcement.

---

<p align="center">
  <a href="./03-why-boundaries-exist.md">◀ Why Boundaries Exist</a>
  &nbsp;|&nbsp;
  <a href="../chapter-03-layers/README.md">Layers ▶</a>
</p>
