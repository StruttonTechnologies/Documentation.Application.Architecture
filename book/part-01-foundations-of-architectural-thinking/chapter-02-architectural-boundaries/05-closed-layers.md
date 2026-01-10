# Closed Layers

Not all layered architectures are equal.

A layered system only becomes architectural when its layers are **closed**—meaning that access is constrained, direction is enforced, and bypassing is not allowed.

This section explains what closed layers are, why they matter, and why open layers quietly erase architectural intent over time.

---

## What a Closed Layer Means

A closed layer enforces a simple rule:

> A layer may only be entered through its defined boundary.

In a closed-layer architecture:
- Higher layers cannot skip lower layers
- Internal details are not visible outside the layer
- All interaction flows through explicit entry points
- Dependencies follow a single, intentional direction

Closed layers turn layering from a diagram into a rule.

---

## Open Layers and the Illusion of Structure

An open layer allows:
- Direct access to internal components
- Bypassing of intended flow
- “Just this once” exceptions

Open layers often look structured at first. Over time, they become indistinguishable from a flat system with naming conventions.

Once a layer can be skipped:
- Responsibility blurs
- Enforcement disappears
- The layer becomes optional

Optional architecture is not architecture.

---

## Closed Layers Protect Responsibility

Each layer exists to own a specific kind of responsibility.

Closed layers ensure that:
- Responsibility stays where it belongs
- Higher layers cannot take shortcuts
- Lower layers are not forced to accommodate misuse
- Changes remain localized

When layers are open, responsibility leaks upward and downward until ownership is unclear.

Closed layers prevent that leakage.

---

## Closed Layers Enable Independent Change

Closed layers allow parts of the system to evolve independently.

Because interaction is constrained:
- Internal changes do not ripple outward
- Implementations can change without breaking consumers
- Testing and reasoning remain localized

This is only possible when layers are protected from direct access.

---

## Why Closed Layers Require Enforcement

Closed layers cannot exist by convention alone.

If the system:
- Allows references that bypass layers
- Permits shared dependencies across layers
- Relies on review or discipline to prevent violations

Then the layers are open in practice, regardless of intent.

Closed layers must be enforced structurally—through dependency rules, physical separation, and explicit contracts.

---

## Why This Matters Later

Later in this book, you will see closed layers expressed through:
- Separate architectural units
- Explicit dependency direction
- Contract-only entry points

Those choices are not stylistic.  
They are the mechanisms that make closed layers real.

Without closed layers, the rest of the architecture collapses into convenience.

---

<p align="center">
  <a href="./04-boundaries-and-layers.md">◀ Boundaries and Layers</a>
  &nbsp;|&nbsp;
  <a href="./06-cqrs-as-a-thinking-model.md">CQRS as a Thinking Model ▶</a>
</p>
