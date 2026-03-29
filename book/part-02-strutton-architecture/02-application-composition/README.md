# Chapter 2 — Application Composition

In the previous chapter, the architecture was introduced at a high level, including how requests move through the system and the key design decisions that shape its structure.

One of the most important of those decisions is how the system is assembled.

Most applications centralize their registration logic in a single location, typically within the application entry point. While this approach is simple, it introduces problems with visibility and architectural control.

This chapter introduces ApplicationComposition.

## In this chapter, you will learn

- what ApplicationComposition is and how it assembles the system  
- how registration is distributed across implementation assemblies  
- how visibility is controlled to enforce architectural boundaries  
- why this approach prevents common architectural failures  

This chapter focuses on how the system is constructed in a way that enforces the architecture rather than relying on convention.

---

[← Back](../01-architecture-overview/03-key-design-decisions.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](01-what-application-composition-is.md)