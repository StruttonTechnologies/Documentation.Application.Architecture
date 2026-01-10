# Chapter 3 — Layers

## Purpose of This Chapter

This chapter establishes layers as an architectural construct for expressing responsibility and controlling dependency direction. While boundaries define where responsibility is separated, layers define how that separation is structured across the system so it can be understood, reasoned about, and sustained as change accumulates. The intent is to build a precise mental model for layering that remains stable regardless of technology, framework, or project structure, and that can be carried forward before any discussion of enforcement or concrete architecture begins.

---

## What This Chapter Covers

- what a layer represents as a zone of responsibility
- how layers introduce and constrain dependency direction
- how layering shapes responsibility and the propagation of change
- why layered systems erode when layers are treated as descriptive rather than constraining
- how misunderstanding layers leads to architectural drift

---

## What This Chapter Does Not Cover

- specific layer names or counts
- project, package, or repository structures
- framework conventions or tooling
- dependency injection, wiring, or configuration
- enforcement mechanisms

---

## How to Read This Chapter

Layers are familiar to most architects, which makes them deceptively easy to misinterpret. Because layering is often introduced early, it is frequently internalized as an organizational or visual pattern rather than as a constraint on responsibility and dependency. Readers should approach this chapter with attention to how layers shape system behavior under pressure, not just how they appear when drawn, with the goal of restoring clarity to a concept that is often assumed rather than examined.

---

## What Comes After This

Once layers are understood as responsibility zones with directional constraints, it becomes possible to introduce a critical limitation. Not all layers should be accessible. The next chapter builds on this foundation by introducing closed layers and explaining how layering moves from intention to enforcement.

---

<p align="center">
  <a href="../chapter-02-architectural-boundaries/README.md">◀ Chapter 2 Overview</a>
  &nbsp;|&nbsp;
  <a href="./01-what-is-a-layer.md">What Is a Layer ▶</a>
</p>
