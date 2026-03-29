# Glossary

## A

### <a id="architecture"></a>Architecture
The structure of a system, including its responsibilities, boundaries, and rules of interaction.

### <a id="applicationcomposition"></a>ApplicationComposition
The composition root responsible for assembling the system by combining all modules and their dependencies into a single application.

---

## B

### <a id="boundary"></a>Boundary
A controlled separation between parts of a system that prevents direct dependency on internal implementation.

---

## C

### <a id="client"></a>Client
Any external system or interface that interacts with the application, such as a web UI, mobile app, or external service.

### <a id="composition-root"></a>Composition Root
The location in the system where dependencies are registered and assembled.

### <a id="contract"></a>Contract
A defined interface that controls how different parts of the system interact.

### <a id="coordinator"></a>Coordinator
The entry point for request execution within the Application layer, responsible for handling commands and queries.

---

## D

### <a id="dependency-direction"></a>Dependency Direction
The rule that dependencies must flow in a controlled and consistent direction across the system.

### <a id="domain"></a>Domain
The core business concepts and rules of the system.

### <a id="dto"></a>DTO (Data Transfer Object)
A data structure used for interaction between system boundaries. DTOs are used for input and output, not execution.

---

## E

### <a id="entity"></a>Entity
A domain representation used for execution within the system. Entities contain meaning and behavior related to the domain.

### <a id="enforcement"></a>Enforcement
The act of structuring the system so that architectural rules are maintained by design rather than by convention.

---

## M

### <a id="mapping"></a>Mapping
The process of transforming DTOs into entities and entities into DTOs.

### <a id="microservices"></a>Microservices
A system composed of independently deployed services that communicate over a network.

### <a id="module"></a>Module
An independent unit of functionality within a system that contains its own internal structure and does not directly depend on other modules.

---

## O

### <a id="orchestration"></a>Orchestration
A component responsible for coordinating multi-step workflows that cannot be completed within a single transaction.

---

## P

### <a id="persistence"></a>Persistence
The mechanism used to store and retrieve data, typically implemented in the Infrastructure layer.

### <a id="presentation-layer"></a>Presentation Layer
The system boundary responsible for receiving requests and returning responses.

### <a id="projection"></a>Projection
A read-focused data shape used to retrieve information without exposing domain entities.

---

## R

### <a id="read-model"></a>Read Model
A representation of data optimized for querying and retrieval rather than modification.

### <a id="repository"></a>Repository
A contract that defines how data is accessed or modified without exposing persistence implementation details.

---

## S

### <a id="service-based-architecture"></a>Service-Based Architecture
A system organized into independent modules within a single deployment, with strong internal separation.

### <a id="single-transaction-model"></a>Single Transaction Model
A request execution pattern where all work is completed within one transaction.

---

## T

### <a id="transaction"></a>Transaction
A unit of work that ensures data changes are applied consistently.

---

## W

### <a id="write-model"></a>Write Model
A representation of data focused on executing changes and enforcing business rules.

### <a id="multi-transaction-workflow"></a>Multi-Transaction Workflow
A coordinated execution pattern involving multiple steps, typically managed by Orchestration.

---

## C (continued)

### <a id="clean-monolith"></a>Clean Monolith
A single deployable application with strong internal architectural boundaries.