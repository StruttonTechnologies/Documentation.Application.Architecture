# Chapter 7 — DTOs, Entities, and Domain Visibility

The previous chapters introduced how requests move through the architecture, how workflows are coordinated, and how persistence responsibilities are isolated behind architectural boundaries.

Throughout those discussions, DTOs and entities have been referenced as different representations of data. This chapter examines those concepts in greater depth and explains why the architecture treats them as distinct responsibilities.

Not all data serves the same purpose. Some representations exist to support interaction with the outside world, while others exist to support business execution within the application. Understanding that distinction is fundamental to maintaining clear architectural boundaries.

This chapter explains how DTOs, entities, and domain visibility work together within the Strutton Technologies Application Architecture.

## In this chapter, you will learn

- the responsibility of DTOs within the architecture
- the responsibility of domain entities
- how domain visibility protects business execution
- why interaction models and domain models remain separate

By the end of this chapter, you will understand how data representations change as requests move through the architecture and why those boundaries are essential to preserving architectural responsibilities.

---

[← Repository and Persistence](../06-repository-and-persistence/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[DTOs and Interaction →](01-dtos-and-interaction.md)