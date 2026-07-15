# What Boundaries Separate

Architectural boundaries separate areas of responsibility within a system.

Each boundary represents a division between two distinct responsibilities. Those responsibilities may exist at different levels of the architecture, but the principle remains the same. What belongs on one side of a boundary should not freely mix with what belongs on the other.

This separation is intentional.

It reflects differences in responsibility.

For example, one area of a system may be responsible for receiving requests, while another is responsible for executing business behavior. These responsibilities should remain distinct because they serve different purposes and change for different reasons.

Architectural boundaries preserve that separation.

They ensure that responsibilities remain contained within their intended area and do not gradually become intertwined with other parts of the system. This makes the architecture easier to understand because every area has a clear and well-defined purpose.

It also makes the system easier to change.

When responsibilities are separated by architectural boundaries, changes can usually be made within one area without producing unintended effects elsewhere in the system.

This is how architectural boundaries preserve clarity, maintain structure, and support the long-term evolution of the system.

---

[← Back](01-what-boundaries-are.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](03-why-boundaries-matter.md)