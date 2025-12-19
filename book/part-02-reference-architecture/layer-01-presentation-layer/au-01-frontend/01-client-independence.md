# Client Independence

## Responsibility

Frontend Architectural Units must remain **independent of one another** and **independent of internal application behavior**.

No frontend technology is architecturally privileged.  
All frontends interact with the system through the same API surface and follow the same rules.

---

## Why This Responsibility Exists

Frontend technologies evolve rapidly.  
Application behavior should not.

If the architecture allows frontend technology to influence system behavior, the system becomes tightly coupled to presentation concerns. Over time, this coupling makes change expensive and risky.

Client Independence exists to ensure that:

- Frontend technology choices remain reversible
- Multiple clients can coexist without conflict
- External integrations follow the same interaction model as internal UIs

This responsibility decouples *how the system is used* from *how the system behaves*.

---

## Architectural Implications

When Client Independence is upheld:

- No frontend has direct knowledge of application orchestration
- No frontend bypasses API-defined entry points
- No frontend embeds assumptions about internal behavior

All clients are treated as **external actors**, regardless of ownership or deployment model.

---

## What This Responsibility Protects

Client Independence protects:

- **Architectural longevity**  
  Frontends can evolve without forcing internal redesign

- **Behavioral consistency**  
  All clients experience the same rules and outcomes

- **Security and policy enforcement**  
  No frontend gains special access by virtue of implementation

- **Organizational scalability**  
  Teams can build and deploy clients independently

---

## Consequences of Violation

When Client Independence is compromised:

- Business logic migrates into the UI
- Different clients produce different outcomes
- Application behavior becomes fragmented
- Architectural boundaries erode silently

Once this happens, restoring architectural integrity is costly and disruptive.

---

## Relationship to Other Responsibilities

Client Independence depends on and reinforces:

- **Execution Delegation**
- **Boundary Enforcement**
- **Contract Stability**

Together, these responsibilities define the frontend’s role as a pure interaction surface.

---

<p align="center">
  <a href="./README.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="./02-execution-delegation.md">Next ▶</a>
</p>
