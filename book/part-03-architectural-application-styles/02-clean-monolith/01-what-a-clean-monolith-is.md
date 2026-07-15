# What a Clean Monolith Is

A monolith is an application deployed as a single unit.

That definition describes deployment, not internal architecture.

A clean monolith is a single deployable application whose internal responsibilities, boundaries, contracts, and dependency rules remain clearly defined and structurally enforced.

The application may run as one process and be released as one unit, but its internal architecture does not collapse into one undifferentiated body of code.

Within a clean monolith:

- responsibilities have clear owners
- layers organize those responsibilities
- boundaries prevent unintended interaction
- contracts expose permitted capabilities
- dependencies follow a controlled direction
- implementation details remain hidden

The architecture presented in Part 2 can operate entirely within this style.

The application remains one deployable system while its internal structure continues to protect the architectural model.

The defining characteristic is not that everything is together.

It is that everything remains structured while being deployed together.

---

[← Chapter Overview](README.md) |
[Table of Contents](../../04-table-of-contents.md) |
[How This Architecture Fits →](02-how-this-architecture-fits.md)
