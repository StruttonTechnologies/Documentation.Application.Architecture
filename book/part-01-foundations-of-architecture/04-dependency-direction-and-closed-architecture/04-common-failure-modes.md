# Common Failure Modes

Dependency direction is often defined but not consistently enforced.

One of the most common failure patterns is allowing dependencies to be introduced wherever they are convenient. What begins as a simple shortcut gradually becomes a network of relationships that no longer reflects the intended architecture.

Another common failure is allowing architectural layers to be bypassed.

Responsibilities begin interacting directly with other responsibilities that were intentionally separated by intermediate layers. While these shortcuts may simplify an individual implementation, they weaken the architectural structure and gradually erode the integrity of the system.

There is also a tendency to relax dependency rules under pressure.

Deadlines, complexity, or convenience can lead to decisions that violate the intended direction of interaction. Although each decision may appear harmless on its own, together they gradually weaken the architecture and make future changes more difficult.

All of these issues lead to the same outcome.

Dependency relationships become increasingly difficult to understand. Architectural boundaries lose their effectiveness. Responsibilities become blurred, changes become less predictable, and confidence in the architecture gradually declines.

Dependency direction only provides value when it is clearly defined, consistently enforced, and supported by an architecture that prevents dependencies from forming in unintended ways.

---

[← Back](03-closed-architecture.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../05-contracts-and-interaction/README.md)