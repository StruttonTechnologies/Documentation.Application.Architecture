# Glossary

## Architecture
The high-level structural design of a software system, including its responsibilities, boundaries, dependency direction, and governing rules.

## Architectural Boundary
A defined separation between parts of a system that controls how responsibilities and dependencies are allowed to interact.

## Clean Monolith
A single deployable application that preserves strong internal structure, clear boundaries, and disciplined dependency direction.

## Contract
A formal interface or defined interaction point between architectural units or layers.

## Coordinator
The architectural unit responsible for handling commands and queries, validating requests, mapping data, and directing single-step application behavior.

## Dependency Direction
The allowed direction in which one part of the system may depend on another.

## Domain
The part of the architecture that represents business concepts, rules, and behavioral integrity.

## DTO
A Data Transfer Object used to move data across architectural boundaries without exposing internal implementation details.

## Infrastructure
The layer responsible for technical implementation concerns such as persistence, framework integration, and external system access.

## Monolith
A single deployable application in which all system parts run together as one deployed unit.

## Microservices
An architectural implementation style composed of multiple independently deployable services that communicate across the network.

## Orchestration
A higher-level coordination mechanism used when a workflow spans multiple steps, operations, or transactional concerns.

## Presentation Layer
The layer responsible for receiving requests and returning responses, without owning core business logic.

## Repository
A persistence-focused abstraction that provides access to stored data while helping keep technical data access concerns out of higher layers.

## Service-Based Monolith
A single deployable application that preserves internal separation between distinct areas of responsibility while still running as one deployed unit.

## Transaction
A controlled unit of work that succeeds or fails as a single consistent operation.

## Unit of Work
A pattern used to coordinate persistence changes and commit them as one transactional boundary.

---

[← Back](06-index.md) | [Table of Contents](04-table-of-contents.md) | [Next →](README.md)
