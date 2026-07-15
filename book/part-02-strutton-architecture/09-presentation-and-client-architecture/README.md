# Chapter 8 — Presentation and Client Architecture

The previous chapters established how the architecture is constructed, how requests are executed, how persistence is isolated, and how architectural representations are protected.

The next architectural responsibility is exposing the system to its consumers.

The architecture deliberately separates business execution from user experience. The API serves as the architectural boundary of the system, while user interfaces act as clients of that boundary rather than extensions of the application itself.

This chapter explains how presentation and client architecture work together while preserving the same architectural boundaries established throughout the rest of the system.

## In this chapter, you will learn

- why the API serves as the architectural boundary
- how user interfaces consume the architecture as clients
- how multiple client applications can share the same business behavior
- why separating presentation from execution improves flexibility and maintainability

By the end of this chapter, you will understand how the architecture supports multiple user experiences without duplicating business behavior or weakening architectural boundaries.

---

[← DTOs, Entities, and Domain Visibility](../07-dtos-entities-and-domain-visibility/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[API as System Boundary →](01-api-as-system-boundary.md)