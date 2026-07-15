# Table of Contents

- [Title](01-title.md)
- [Copyright](02-copyright.md)
- [Preface](03-preface.md)
- [Introduction](05-introduction.md)
- [Index](06-index.md)
- [Glossary](07-glossary.md)

---

# Part 1 — Foundations of Architecture

## 01 — What Is Software Architecture
- [Definition and Purpose](part-01-foundations-of-architecture/01-what-is-software-architecture/01-definition-and-purpose.md)
- [Where Systems Fail](part-01-foundations-of-architecture/01-what-is-software-architecture/02-where-systems-fail.md)
- [Architecture in Code](part-01-foundations-of-architecture/01-what-is-software-architecture/03-architecture-in-code.md)
- [Why Architecture Matters](part-01-foundations-of-architecture/01-what-is-software-architecture/04-why-architecture-matters.md)
- [What Architecture Is Not](part-01-foundations-of-architecture/01-what-is-software-architecture/05-what-architecture-is-not.md)

## 02 — Architectural Layers
- [What Layers Are](part-01-foundations-of-architecture/02-architectural-layers/01-what-layers-are.md)
- [What Layers Are Not](part-01-foundations-of-architecture/02-architectural-layers/02-what-layers-are-not.md)
- [Why Layers Matter](part-01-foundations-of-architecture/02-architectural-layers/03-why-layers-matter.md)
- [Common Failure Modes](part-01-foundations-of-architecture/02-architectural-layers/04-common-failure-modes.md)

## 03 — Architectural Boundaries
- [What Boundaries Are](part-01-foundations-of-architecture/03-architectural-boundaries/01-what-boundaries-are.md)
- [What Boundaries Separate](part-01-foundations-of-architecture/03-architectural-boundaries/02-what-boundaries-separate.md)
- [Why Boundaries Matter](part-01-foundations-of-architecture/03-architectural-boundaries/03-why-boundaries-matter.md)
- [Common Failure Modes](part-01-foundations-of-architecture/03-architectural-boundaries/04-common-failure-modes.md)

## 04 — Dependency Direction and Closed Architecture
- [What Dependency Direction Is](part-01-foundations-of-architecture/04-dependency-direction-and-closed-architecture/01-what-dependency-direction-is.md)
- [Why Direction Matters](part-01-foundations-of-architecture/04-dependency-direction-and-closed-architecture/02-why-direction-matters.md)
- [Closed Architecture](part-01-foundations-of-architecture/04-dependency-direction-and-closed-architecture/03-closed-architecture.md)
- [Common Failure Modes](part-01-foundations-of-architecture/04-dependency-direction-and-closed-architecture/04-common-failure-modes.md)

## 05 — Contracts and Interaction
- [What Contracts Are](part-01-foundations-of-architecture/05-contracts-and-interaction/01-what-contracts-are.md)
- [Contracts vs Implementation](part-01-foundations-of-architecture/05-contracts-and-interaction/02-contracts-vs-implementation.md)
- [Why Contracts Matter](part-01-foundations-of-architecture/05-contracts-and-interaction/03-why-contracts-matter.md)
- [Common Failure Modes](part-01-foundations-of-architecture/05-contracts-and-interaction/04-common-failure-modes.md)

## Part 1 Summary
- [Summary](part-01-foundations-of-architecture/99-part-01-summary/README.md)

---

# Part 2 — Strutton Technologies Application Architecture

## 01 — Architecture Overview
- [High-Level Structure](part-02-strutton-architecture/01-architecture-overview/01-high-level-structure.md)
- [Request Flow](part-02-strutton-architecture/01-architecture-overview/02-request-flow.md)
- [Key Design Decisions](part-02-strutton-architecture/01-architecture-overview/03-key-design-decisions.md)

## 02 — Application Composition
- [What Application Composition Is](part-02-strutton-architecture/02-application-composition/01-what-application-composition-is.md)
- [Distributed Registration](part-02-strutton-architecture/02-application-composition/02-distributed-registration.md)
- [Controlled Visibility](part-02-strutton-architecture/02-application-composition/03-controlled-visibility.md)
- [Why This Matters](part-02-strutton-architecture/02-application-composition/04-why-this-matters.md)
- [Common Failure Modes](part-02-strutton-architecture/02-application-composition/05-common-failure-modes.md)

## 03 — Request Entry and Coordinator Contracts
- [Request Entry](part-02-strutton-architecture/03-request-entry-and-coordinator-contracts/01-request-entry.md)
- [Coordinator Contracts](part-02-strutton-architecture/03-request-entry-and-coordinator-contracts/02-coordinator-contracts.md)
- [Controlled Access to Execution](part-02-strutton-architecture/03-request-entry-and-coordinator-contracts/03-controlled-access-to-execution.md)
- [Why This Matters](part-02-strutton-architecture/03-request-entry-and-coordinator-contracts/04-why-this-matters.md)
- [Common Failure Modes](part-02-strutton-architecture/03-request-entry-and-coordinator-contracts/05-common-failure-modes.md)

## 04 — Coordinator Implementation
- [Role of the Coordinator](part-02-strutton-architecture/04-coordinator-implementation/01-role-of-the-coordinator.md)
- [Handlers and Execution](part-02-strutton-architecture/04-coordinator-implementation/02-handlers-and-execution.md)
- [Validation and Mapping](part-02-strutton-architecture/04-coordinator-implementation/03-validation-and-mapping.md)
- [DTO to Entity Transition](part-02-strutton-architecture/04-coordinator-implementation/04-dto-to-entity-transition.md)
- [Common Failure Modes](part-02-strutton-architecture/04-coordinator-implementation/05-common-failure-modes.md)

## 05 — Orchestration
- [What Orchestration Is](part-02-strutton-architecture/05-orchestration/01-what-orchestration-is.md)
- [When Orchestration Is Used](part-02-strutton-architecture/05-orchestration/02-when-orchestration-is-used.md)
- [When Orchestration Is Not Used](part-02-strutton-architecture/05-orchestration/03-when-orchestration-is-not-used.md)
- [How Orchestration Works](part-02-strutton-architecture/05-orchestration/04-how-orchestration-works.md)
- [Common Failure Modes](part-02-strutton-architecture/05-orchestration/05-common-failure-modes.md)

## 06 — Repository and Persistence
- [Repository Contracts](part-02-strutton-architecture/06-repository-and-persistence/01-repository-contracts.md)
- [Persistence Abstraction](part-02-strutton-architecture/06-repository-and-persistence/02-persistence-abstraction.md)
- [Commit and Transaction Boundaries](part-02-strutton-architecture/06-repository-and-persistence/03-commit-and-transaction-boundaries.md)
- [How It Fits Together](part-02-strutton-architecture/06-repository-and-persistence/04-how-it-fits-together.md)
- [Common Failure Modes](part-02-strutton-architecture/06-repository-and-persistence/05-common-failure-modes.md)

## 07 — DTOs, Entities, and Domain Visibility
- [DTOs and Interaction](part-02-strutton-architecture/07-dtos-entities-and-domain-visibility/01-dtos-and-interaction.md)
- [Entities and Execution](part-02-strutton-architecture/07-dtos-entities-and-domain-visibility/02-entities-and-execution.md)
- [Domain Visibility Rules](part-02-strutton-architecture/07-dtos-entities-and-domain-visibility/03-domain-visibility-rules.md)
- [Why This Matters](part-02-strutton-architecture/07-dtos-entities-and-domain-visibility/04-why-this-matters.md)
- [Common Failure Modes](part-02-strutton-architecture/07-dtos-entities-and-domain-visibility/05-common-failure-modes.md)

## 08 — Presentation and Client Architecture
- [API as the System Boundary](part-02-strutton-architecture/08-presentation-and-client-architecture/01-api-as-system-boundary.md)
- [UI as a Client](part-02-strutton-architecture/08-presentation-and-client-architecture/02-ui-as-client.md)
- [Supporting Multiple User Experiences](part-02-strutton-architecture/08-presentation-and-client-architecture/03-supporting-multiple-user-experiences.md)
- [Why This Matters](part-02-strutton-architecture/08-presentation-and-client-architecture/04-why-this-matters.md)
- [Common Failure Modes](part-02-strutton-architecture/08-presentation-and-client-architecture/05-common-failure-modes.md)

## 09 — Architectural Enforcement
- [Why Enforcement Matters](part-02-strutton-architecture/09-architectural-enforcement/01-why-enforcement-matters.md)
- [How the Architecture Enforces Itself](part-02-strutton-architecture/09-architectural-enforcement/02-how-the-architecture-enforces-itself.md)
- [What This Prevents](part-02-strutton-architecture/09-architectural-enforcement/03-what-this-prevents.md)
- [Long-Term Impact](part-02-strutton-architecture/09-architectural-enforcement/04-long-term-impact.md)

## Part 2 Summary
- [Summary](part-02-strutton-architecture/99-part-02-summary/README.md)

---

# Part 3 — Architectural Application Styles

## 01 — Applying Architecture at Scale
- [Architecture vs Deployment](part-03-architectural-application-styles/01-applying-architecture-at-scale/01-architecture-vs-deployment.md)
- [What Scaling Really Means](part-03-architectural-application-styles/01-applying-architecture-at-scale/02-what-scaling-really-means.md)
- [How Structure Evolves](part-03-architectural-application-styles/01-applying-architecture-at-scale/03-how-structure-evolves.md)
- [Common Misconceptions](part-03-architectural-application-styles/01-applying-architecture-at-scale/04-common-misconceptions.md)

## 02 — Clean Monolith
- [What a Clean Monolith Is](part-03-architectural-application-styles/02-clean-monolith/01-what-a-clean-monolith-is.md)
- [How This Architecture Fits](part-03-architectural-application-styles/02-clean-monolith/02-how-this-architecture-fits.md)
- [Why It Works](part-03-architectural-application-styles/02-clean-monolith/03-why-it-works.md)
- [When It Breaks Down](part-03-architectural-application-styles/02-clean-monolith/04-when-it-breaks-down.md)

## 03 — Service-Based Architecture
- [What Service-Based Architecture Is](part-03-architectural-application-styles/03-service-based-architecture/01-what-service-based-architecture-is.md)
- [How It Differs from a Clean Monolith](part-03-architectural-application-styles/03-service-based-architecture/02-how-it-differs-from-a-clean-monolith.md)
- [Why Modules Matter](part-03-architectural-application-styles/03-service-based-architecture/03-why-modules-matter.md)
- [Where It Gets More Complex](part-03-architectural-application-styles/03-service-based-architecture/04-where-it-gets-more-complex.md)

## 04 — Microservices
- [What Microservices Are](part-03-architectural-application-styles/04-microservices/01-what-microservices-are.md)
- [How the Architecture Applies](part-03-architectural-application-styles/04-microservices/02-how-the-architecture-applies.md)
- [What You Gain](part-03-architectural-application-styles/04-microservices/03-what-you-gain.md)
- [What It Costs](part-03-architectural-application-styles/04-microservices/04-what-it-costs.md)

## 05 — What Changes and What Stays the Same
- [What Stays the Same](part-03-architectural-application-styles/05-what-changes-and-what-stays-the-same/01-what-stays-the-same.md)
- [What Changes](part-03-architectural-application-styles/05-what-changes-and-what-stays-the-same/02-what-changes.md)
- [Why This Distinction Matters](part-03-architectural-application-styles/05-what-changes-and-what-stays-the-same/03-why-this-distinction-matters.md)

## 06 — Choosing the Right Style
- [Start with the Simplest Structure](part-03-architectural-application-styles/06-choosing-the-right-style/01-start-with-the-simplest-structure.md)
- [Signals That You Need More Structure](part-03-architectural-application-styles/06-choosing-the-right-style/02-signals-that-you-need-more-structure.md)
- [When Distribution Becomes Necessary](part-03-architectural-application-styles/06-choosing-the-right-style/03-when-distribution-becomes-necessary.md)
- [Avoiding Common Mistakes](part-03-architectural-application-styles/06-choosing-the-right-style/04-avoiding-common-mistakes.md)

## Part 3 Summary
- [Summary](part-03-architectural-application-styles/99-part-03-summary/README.md)

---

[← Back](README.md) | [Table of Contents](04-table-of-contents.md) | [Next →](part-01-foundations-of-architecture/README.md)