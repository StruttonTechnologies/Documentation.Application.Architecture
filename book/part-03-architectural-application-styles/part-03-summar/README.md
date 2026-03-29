# Part 3 — Summary

This part explored how the architecture can be applied across different system styles.

The goal was not to introduce new architectural concepts, but to show how the same principles adapt as systems grow in size and complexity.

Clean monoliths, service-based systems, and microservices are often treated as fundamentally different approaches.

They are not.

They are different ways of organizing and deploying the same architectural model.

A clean monolith applies the architecture within a single deployable system. A service-based architecture introduces stronger internal separation through modules. Microservices extend those boundaries into independently deployed systems.

In each case, the architecture remains the same.

Responsibilities are still defined. Boundaries are still enforced. Contracts still control interaction. The separation between interaction and execution still applies.

What changes is how those principles are realized.

As systems grow, boundaries become more explicit. Communication becomes more complex. Operational concerns increase. These are consequences of scale, not changes in architecture.

## What This Means

Architecture should not be chosen based on trends.

It should be chosen based on the needs of the system.

Starting with a clean monolith is often the most effective approach. As complexity increases, stronger modular structure may be introduced. Distribution should only be considered when it is required.

The architecture is designed to support this evolution.

It does not need to be replaced as the system grows. It needs to be applied consistently.

## What Comes Next

The next volume focuses on implementation.

It will show how to build systems using this architecture, including project structure, composition, and practical development patterns.

Where this part explained how architecture adapts, the next will show how to apply it in practice.

---

[← Back](../06-choosing-the-right-style/04-avoiding-common-mistakes.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../../README.md)