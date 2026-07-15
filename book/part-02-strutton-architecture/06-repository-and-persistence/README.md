# Chapter 6 — Repository and Persistence

The previous chapter introduced Orchestration and explained how complex workflows are coordinated while preserving architectural boundaries.

Eventually, every business operation reaches a point where information must be stored, retrieved, or modified.

Persistence is a fundamental responsibility of every application, but it should not become the responsibility of every architectural unit.

This chapter introduces the Repository and Persistence architectural units and explains how the architecture isolates persistence behind explicit contracts while preserving the separation between business execution and data access.

## In this chapter, you will learn

- the responsibility of repository contracts
- how persistence is separated from business execution
- how transaction boundaries are owned and controlled
- how repository contracts, persistence, and transaction ownership work together
- why persistence is treated as its own architectural responsibility

By the end of this chapter, you will understand how the architecture performs persistence without exposing implementation details or weakening its architectural boundaries.

---

[← Orchestration](../05-orchestration/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Repository Contracts →](01-repository-contracts.md)