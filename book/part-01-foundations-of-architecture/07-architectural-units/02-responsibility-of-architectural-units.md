# Responsibility of Architectural Units

Architectural units have two primary responsibilities.

The first is to contain behavior.

Each unit is responsible for holding the logic that belongs to a specific area of responsibility. This keeps related behavior together and prevents it from spreading across the system.

The second is to enforce boundaries.

Architectural units ensure that only allowed interactions occur. They prevent unauthorized dependencies and protect the separation between different areas of the system.

These responsibilities work together.

Containing behavior without enforcing boundaries leads to leakage. Enforcing boundaries without clearly containing behavior leads to confusion about where logic belongs.

Architectural units provide both.

They define where behavior exists and ensure that it remains within the intended structure.

---

[← Back](01-what-architectural-units-are.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-architectural-units-matter.md)