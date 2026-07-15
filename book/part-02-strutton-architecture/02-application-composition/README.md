# Chapter 2 — Application Composition

The previous chapter introduced the architecture as a whole. It established the overall structure of the system, demonstrated how requests move through the architecture, and introduced the architectural principles that guide every design decision.

This chapter explores the first architectural unit in detail.

ApplicationComposition is responsible for assembling the application while preserving the architectural boundaries established throughout the system. It serves as the single composition point where independently developed architectural units are brought together to form a complete application.

Rather than simply describing how the system is assembled, this chapter explains why the composition of the application is itself an architectural responsibility and how it contributes to preserving the integrity of the architecture.

## In this chapter, you will learn

- what ApplicationComposition is and the responsibility it owns
- why application composition is treated as an architectural concern
- how composition supports architectural boundaries and controlled visibility
- how the architecture uses composition to reinforce its own rules

By the end of this chapter, you will understand why the composition of an application is more than a startup concern—it is a fundamental part of preserving the architecture itself.

---

[← Architecture Overview](../01-architecture-overview/03-architectural-principles.md) |
[Table of Contents](../../04-table-of-contents.md) |
[What Is ApplicationComposition? →](01-what-application-composition-is.md)