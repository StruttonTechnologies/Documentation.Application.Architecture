# Handler Scope and Discipline

## Responsibility

Handlers are responsible for **coordinating execution without owning business behavior**.

They validate intent, translate representations, route execution, and return results—but they do not implement business rules or coordinate workflows internally.

---

## Why This Responsibility Exists

Handlers are often misused as convenient places to “just add logic.”

Without clear discipline, they accumulate business rules, workflow coordination, and technical concerns, becoming difficult to reason about and change.

Handler Scope and Discipline exist to ensure that:

- Handlers remain focused and readable
- Business rules live in the domain
- Workflows live in orchestration
- Execution flow remains intentional

---

## Architectural Implications

When handler scope is disciplined:

- Handlers are small and predictable
- Complexity is elevated appropriately
- Domain purity is preserved
- Testing remains straightforward

Handlers become **execution coordinators**, not logic containers.

---

## What This Responsibility Protects

Handler Scope and Discipline protect:

- **Architectural clarity**  
  Responsibilities are easy to locate

- **Change safety**  
  Logic changes occur in the correct layer

- **Long-term maintainability**  
  Handlers do not become bottlenecks

- **Execution consistency**  
  All behavior follows the same execution model

---

## Consequences of Violation

When handlers lose discipline:

- Business logic leaks upward
- Workflows are duplicated
- Handlers become bloated
- Architectural boundaries erode

Eventually, the Application layer becomes indistinguishable from the Domain or Infrastructure.

---

## Relationship to Other Responsibilities

Handler Scope and Discipline reinforce:

- **Execution Gateway**  
  Gateways require disciplined coordinators

- **Validation and Routing**  
  Clear routing prevents scope creep

- **Domain Purity**  
  Business rules remain where they belong

Together, these responsibilities ensure that the Dispatcher remains lean, intentional, and architecturally sound.

---

<p align="center">
  <a href="./02-validation-and-routing.md">◀ Back</a>
  &nbsp;|&nbsp;
  <a href="../../../index.md">Index</a>
  &nbsp;|&nbsp;
  <a href="../au-04-orchestration-contracts/README.md">Next ▶</a>
</p>
