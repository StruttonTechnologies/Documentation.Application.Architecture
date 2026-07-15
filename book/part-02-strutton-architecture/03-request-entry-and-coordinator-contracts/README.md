# Chapter 3 — Request Entry and Coordinator Contracts

The previous chapter introduced ApplicationComposition and explained how the application is assembled while preserving architectural boundaries through controlled visibility.

Once the application has been assembled, the next question naturally follows:

**How does a request enter the architecture?**

This chapter introduces Coordinator contracts, the architectural entry point through which all requests enter the Application layer. Rather than exposing execution directly, Coordinator contracts define the interactions that are intentionally made available to the rest of the application.

## In this chapter, you will learn

- how requests enter the architecture
- the responsibility of Coordinator contracts
- how Coordinator contracts preserve controlled visibility
- why execution begins through contracts rather than implementation

By the end of this chapter, you will understand why request entry is treated as an architectural responsibility and how Coordinator contracts reinforce the boundaries established by the architecture.

---

[← Application Composition](../02-application-composition/05-common-architectural-mistakes.md) |
[Table of Contents](../../04-table-of-contents.md) |
[Request Entry →](01-request-entry.md)