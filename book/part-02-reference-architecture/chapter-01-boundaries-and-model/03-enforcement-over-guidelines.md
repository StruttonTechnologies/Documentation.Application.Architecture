# Enforcement Over Guidelines

Architectural rules are only as effective as their enforcement.

Guidelines, conventions, and best practices describe *intent*, but they do not prevent
violation. In small systems or highly disciplined teams, this may be sufficient. In
real-world systems with time pressure, turnover, and evolving requirements, it is not.

This architecture prioritizes **enforcement over guidance**.

---

## The Limits of Guidelines

Guidelines assume:
- consistent interpretation
- shared understanding
- sustained discipline
- careful code review

Over time, those assumptions fail.

Common phrases begin to appear:
- “Just this once”
- “We’ll clean it up later”
- “It’s faster this way”
- “We already have access to it”

None of these indicate bad intent. They indicate an architecture that relies on memory
and restraint instead of structure.

---

## Enforcement Changes the Failure Mode

An enforced architecture does not rely on developers *remembering* the rules.

Instead:
- violations are difficult or impossible
- incorrect dependencies fail at compile time
- responsibility leaks require deliberate effort
- shortcuts are visible and explicit

This shifts the failure mode from *accidental* to *intentional*.

Intentional violations can be discussed and justified. Accidental ones quietly
accumulate.

---

## What Enforcement Looks Like in Practice

In this architecture, enforcement is achieved through s
