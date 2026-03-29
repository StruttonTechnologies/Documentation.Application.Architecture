# Role of the Coordinator

The Coordinator is responsible for handling incoming requests.

It serves as the entry point for execution within the Application layer. Requests that enter the system as commands or queries are processed here.

The Coordinator does not define business rules.

Its responsibility is to manage the execution of a request. It determines how the request should be processed and ensures that it follows the architectural structure.

This includes:

- validating the request  
- mapping input data into domain representations  
- invoking the appropriate operations  
- returning results  

The Coordinator is intentionally limited in scope.

It does not manage complex workflows or coordinate multiple transactions. Those responsibilities belong to the Orchestration layer.

By keeping the Coordinator focused, the architecture maintains clear separation between simple request handling and more complex execution patterns.

---

[← Back](README.md) | [Table of Contents](../../04-table-of-contents.md) | [Next →](02-handlers-and-execution.md)