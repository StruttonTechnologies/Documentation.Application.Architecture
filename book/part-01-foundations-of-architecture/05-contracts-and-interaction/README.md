# Chapter 5 — Contracts and Interaction

In the previous chapters, architectural layers were introduced as a way of organizing responsibilities, architectural boundaries were introduced as a way of protecting those responsibilities, and dependency direction was introduced as a way of controlling how responsibilities are allowed to interact.

The next step is understanding how those interactions are defined.

Architecture does not only determine where responsibilities belong or how they interact. It also defines the agreements that govern communication between them. These agreements are known as architectural contracts.

This chapter introduces contracts as the mechanism that regulates interaction between architectural responsibilities.

## In this chapter, you will learn

- what architectural contracts are
- how contracts define and regulate interaction
- how contracts differ from implementation
- the distinction between internal and external contracts
- why contracts are essential for preserving architectural structure
- common misconceptions and failure patterns involving contracts

This chapter does not focus on specific programming constructs or technologies.

Instead, it establishes the conceptual role contracts play in governing interaction while preserving the architectural boundaries introduced in the previous chapters.

---

[← Back](../04-dependency-direction-and-closed-architecture/04-common-failure-modes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Contracts Are →](01-what-contracts-are.md)