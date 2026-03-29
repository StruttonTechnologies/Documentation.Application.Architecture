# Common Failure Modes

Architectural units are often treated as organizational rather than structural.

One common issue is failing to enforce boundaries within units. Code is allowed to depend on areas it should not, weakening the separation between responsibilities.

Another failure mode is unclear responsibility.

If it is not obvious what belongs within a unit, developers will make inconsistent decisions. This leads to confusion and scattered logic.

There is also a tendency to bypass architectural units entirely.

Shortcuts are taken to access functionality directly instead of going through the intended structure. These shortcuts accumulate, eroding the architecture over time.

All of these issues lead to the same outcome.

The system becomes harder to understand, harder to maintain, and less aligned with its intended structure.

Architectural units only provide value when they are clearly defined and consistently enforced.

---

[← Back](03-why-architectural-units-matter.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](../../part-02-your-architecture/README.md)