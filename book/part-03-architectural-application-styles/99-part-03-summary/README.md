# Part 3 — Summary

This part examined how the Strutton Technologies Application Architecture applies across different application styles.

The goal was not to introduce a replacement architecture for each style. It was to show that clean monoliths, service-based systems, and microservices can preserve the same underlying architectural principles.

Architecture and deployment are not the same.

Architecture defines responsibilities, boundaries, contracts, dependency direction, and enforcement. Application style determines how those responsibilities are grouped, how strongly their boundaries are represented, and how the system is deployed and operated.

A clean monolith preserves the complete architecture within one deployable application.

A service-based architecture strengthens business ownership through explicit modules or larger services while avoiding unnecessary fine-grained distribution.

Microservices extend selected architectural boundaries into independently deployed services and accept the communication, consistency, and operational costs that independence requires.

Across all three styles, the architecture remains consistent.

- every significant responsibility has a clear owner
- boundaries protect those responsibilities
- contracts regulate interaction
- dependency direction remains controlled
- internal implementation remains hidden
- the structure of the system continues to enforce the intended architecture

What changes is how those principles are realized.

Boundaries may become more explicit. Communication may move from in-process calls to distributed interaction. Transaction scope may narrow. Deployment, operation, and team ownership may become independent.

These changes should be introduced only when demonstrated needs justify their cost.

## What This Means

Application style should not be selected by trend, prestige, or anticipated scale.

The strongest default is the simplest style capable of preserving architectural integrity and satisfying the current needs of the system.

Begin with clear responsibilities and enforceable boundaries.

Strengthen modular organization when growth requires clearer ownership.

Introduce distribution only when independent deployment or operation provides measurable value that outweighs its permanent complexity.

The architecture does not need to be replaced as the system evolves.

It must be applied consistently as the form of the system changes.

## What Comes Next

This volume has defined the foundational concepts, presented the Strutton Technologies Application Architecture, and examined how that architecture applies across different application styles.

Implementation and engineering practices are intentionally outside its scope.

Future volumes can address how the architecture is constructed in specific technologies and how production software is supported through disciplines such as configuration, logging, caching, messaging, testing, observability, security, and operations.

The architectural model is now complete.

---

[← Choosing the Right Style](../06-choosing-the-right-style/04-avoiding-common-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Return to Book Overview →](../../README.md)
