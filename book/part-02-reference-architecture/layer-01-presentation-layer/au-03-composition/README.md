# AU-03 — Composition & Dependency Injection

## Overview

The Composition & Dependency Injection Architectural Unit defines **how the application is assembled at runtime**.

This AU describes how services from multiple layers are wired together to form a complete, executable application, while preserving architectural boundaries and dependency direction.

In this architecture, composition is centralized, explicit, and confined to the Presentation layer.

This location serves as the **composition root** of the application.

The composition root is the only place where implementations from multiple layers are known and assembled together. By confining this responsibility to a single location, the architecture ensures that dependency direction, boundary enforcement, and startup behavior remain explicit and enforceable.

---

## The Role of Composition

Composition exists to:

- Assemble implementations from multiple layers
- Bind contracts to concrete types
- Produce the final application object graph
- Keep startup logic isolated from behavior

It answers the question:

> “How does the application become runnable?”

—not—

> “What does the application do?”  
> “How are use cases executed?”  
> “Where does business logic live?”

---

## What Belongs in This AU

This Architectural Unit contains:

- Layer-specific registration mechanisms
- Centralized service aggregation
- Startup composition logic
- Application entry-point wiring

Composition code may reference multiple layers, but it contains **no application behavior**.

---

## What Does Not Belong Here

Composition deliberately excludes:

- Business logic
- Use-case orchestration
- Domain rules
- Infrastructure implementations
- Runtime decision-making

It assembles behavior; it does not define it.

---

## What You Will Learn in This AU

The pages in this AU explain:

- Why each layer exposes its own registrar
- How registrations are aggregated safely
- Why composition is centralized
- How the application entry point remains thin

---

## Topics in This AU

- [01 — Layer Registrars](01-layer-registrars.md)
- [02 — Centralized Composition](02-centralized-composition.md)
- [03 — Program Entry Point](03-program-entry-point.m)
