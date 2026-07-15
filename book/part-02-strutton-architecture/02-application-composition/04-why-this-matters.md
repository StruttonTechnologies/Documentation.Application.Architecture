# Why This Matters

Without controlled composition, architectural boundaries become easy to bypass.

In many applications, the application entry point references implementation assemblies directly. As additional assemblies are introduced, the entry point gradually becomes aware of more and more of the system's internal structure.

While this approach may appear convenient, it weakens the architecture.

Developers can unintentionally introduce dependencies that skip architectural boundaries, bypass contracts, or access implementation details directly. Over time, these shortcuts increase coupling, reduce maintainability, and gradually erode the intended structure of the system.

ApplicationComposition prevents this.

By controlling how the application is assembled and limiting visibility to implementation assemblies, it reinforces the intended architectural boundaries and ensures that interaction follows approved architectural paths.

The result is a more consistent architecture.

Rather than relying solely on developer discipline to preserve architectural integrity, the structure of the application reinforces the architectural rules automatically wherever practical.

---

[← Controlled Visibility](03-controlled-visibility.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Common Failure Modes →](05-common-architectural-mistakes.md)