# Common Failure Modes

Layered architectures rarely fail because the concept is wrong. They fail because the intent behind layering is slowly eroded by reasonable decisions made under pressure. These failures are usually incremental, often invisible while they are happening, and only obvious in hindsight. This page exists to surface those patterns so they can be recognized and corrected before they become systemic.

---

## Layers Become Labels Instead of Constraints

One of the most common failure modes occurs when layers are treated as descriptive labels rather than architectural constraints. The system may appear layered in diagrams or solution structure, but behavior is not meaningfully restricted. Dependencies form wherever they are convenient, and responsibility becomes negotiable.

This failure often appears as:
- layers that exist in name but do not restrict interaction
- direct dependencies that bypass intended structure
- debates about whether a violation is “really that bad”
- diagrams that look correct while code behaves otherwise

When layers do not constrain behavior, they cease to function as architecture.

---

## Responsibility Drifts Across Layers

Layers fail when responsibility is allowed to move without explicit decision. Over time, logic accumulates where it is easiest to place, not where it belongs. This drift is rarely malicious. It usually happens in response to deadlines, incidents, or incomplete understanding.

Signs of responsibility drift include:
- business rules appearing in multiple layers
- infrastructure concerns leaking upward
- orchestration logic spreading across unrelated components
- changes requiring coordination across many layers

When responsibility is unclear, change becomes expensive and unpredictable.

---

## Direction Becomes Optional

Another failure mode emerges when dependency direction is treated as guidance rather than rule. Once exceptions are allowed, they tend to multiply. Each exception feels justified in isolation, but collectively they erase the benefits layering was meant to provide.

This erosion typically shows up as:
- “temporary” backward dependencies
- shared models introduced to reduce duplication
- circular dependencies rationalized as edge cases
- enforcement deferred until later and never revisited

Direction that can be ignored under pressure is not direction.

---

## Layers Are Inferred Instead of Defined

Some systems attempt to discover layers by analyzing existing code rather than defining them deliberately. In these cases, layers become an explanation of current structure instead of a constraint on future change. Architecture shifts from a design activity to a documentation exercise.

This failure often looks like:
- reverse engineering layers from repository layout
- redefining layers after major refactors
- treating architecture as an emergent property
- adjusting conceptual models to fit existing code

Architecture must lead. Code must follow.

---

## Enforcement Is Deferred Indefinitely

A final and particularly damaging failure mode occurs when enforcement is acknowledged but postponed. Teams agree on layering in principle, but violations are tolerated with the intention of fixing them later. Over time, those violations become embedded, and enforcement becomes politically or technically difficult.

This pattern commonly includes:
- planned cleanups that never happen
- architectural debt tracked but never retired
- rules applied inconsistently across teams
- enforcement introduced only after problems escalate

Architecture that relies on future discipline is fragile by design.

---

## Why These Failures Persist

None of these failure modes stem from ignorance or incompetence. They emerge because layered architecture requires continuous clarity and intentional enforcement. Without both, systems naturally evolve toward convenience, coupling, and ambiguity.

Recognizing these patterns early is one of the most important responsibilities of an architect.

---

<p align="center">
  <a href="./02-what-a-layer-is-not.md">◀ What a Layer Is Not</a>
  &nbsp;|&nbsp;
  <a href="../chapter-04-closed-layers/README.md">Closed Layers ▶</a>
</p>
