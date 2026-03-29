# Entities and Execution

Entities are used for execution.

They represent domain concepts and are used within the system to perform operations. Entities carry meaning within the domain and define how the system behaves.

Entities are not exposed externally.

They are created within the Coordinator after mapping from DTOs and are used throughout execution.

This separation is intentional.

It ensures that execution logic operates on domain representations rather than data structures designed for interaction.

Entities remain within the internal boundaries of the system.

They are not used for communication with external clients.