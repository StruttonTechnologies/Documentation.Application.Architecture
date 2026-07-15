# What Boundaries Are

Architectural boundaries define the separation between responsibilities within a system.

While architectural layers organize responsibilities, boundaries protect them by defining where one area of responsibility ends and another begins. They establish the limits that prevent responsibilities from gradually spreading throughout the system.

A boundary is not a physical barrier.

It is a conceptual constraint that governs how different parts of a system are allowed to interact. It defines what information, behavior, or communication may cross from one area of responsibility to another and what must remain contained.

This distinction is fundamental.

Without architectural boundaries, layers lose their effectiveness. Responsibilities may be organized into separate layers, but nothing prevents those responsibilities from leaking across the architecture. Over time, the structure gradually erodes because it is no longer being protected.

Architectural boundaries preserve the integrity of the system.

They ensure that responsibilities remain where they belong and that interactions between different areas of the architecture are deliberate, controlled, and predictable.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-what-boundaries-separate.md)