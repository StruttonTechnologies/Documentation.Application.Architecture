# DTOs and Interaction

DTOs are used for interaction.

They define the shape of data as it enters and exits the system. DTOs are designed for communication, not execution.

They represent external input and output.

This allows the system to control how data is received and returned without exposing internal structures.

DTOs exist at the boundary of the system.

They are used in the Presentation layer and passed into the Application layer, where they are processed by the Coordinator.

DTOs do not represent domain concepts.

They are shaped for interaction and may change based on how the system is used, without affecting the core behavior of the system.