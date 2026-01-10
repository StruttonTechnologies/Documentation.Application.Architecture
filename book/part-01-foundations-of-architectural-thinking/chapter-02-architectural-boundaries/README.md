# Chapter 2 — Architectural Boundaries

## Purpose of This Chapter

This chapter introduces the most important concept in this book.

Before we discuss layers, contracts, or system structure, we must first understand **architectural boundaries**. Boundaries are where architecture stops being conceptual and becomes real. They define responsibility, control knowledge flow, and determine whether an architecture can be enforced or merely suggested.

If boundaries are unclear, everything that follows—layers, patterns, and even code quality—will be unstable.

---

## Why Boundaries Come First

Many architects are taught to start with layers or patterns. That ordering is backwards.

Layers, services, and components are all *expressions* of boundaries. If you do not first understand where boundaries exist and what they protect, those structures become arbitrary.

Boundaries answer questions that layers alone cannot:
- Where does responsibility begin and end?
- What knowledge is allowed to cross?
- What must never cross?
- What happens when pressure pushes against the structure?

This chapter establishes boundaries as the foundation upon which all other architectural decisions are built.

---

## What This Chapter Covers

In this chapter, we will explore:

- What an architectural boundary is
- What a boundary is not
- Why boundaries exist in software systems
- How boundaries control responsibility and knowledge
- Why unenforced boundaries eventually disappear

These concepts are presented without reference to specific frameworks, technologies, or implementations. The focus is on architectural reasoning, not mechanics.

---

## What This Chapter Does *Not* Cover

This chapter intentionally avoids:

- Project structures or repository layouts
- APIs, services, or communication protocols
- Specific architectural styles
- Tooling or enforcement mechanisms
- Concrete examples from the final architecture

Those details come later. This chapter is about *thinking clearly* about boundaries before we name or implement them.

---

## How to Read This Chapter

This chapter is written deliberately and slowly.

If you are new to architecture, take time to internalize the ideas before moving on.  
If you are experienced, resist the urge to map these concepts immediately to past systems.

This chapter is not asking whether boundaries *can* exist.  
It is asking whether boundaries are **real** in your architecture.

---

## What Comes After This

Once we are clear on what boundaries are and why they matter, we can begin to explore how boundaries are expressed structurally—starting with layers and direction of dependency.

But first, we must answer a simple question:

**What is an architectural boundary?**

---

<p align="center">
  <a href="../chapter-01-what-architecture-is-and-is-not/README.md">◀ Chapter 1 Overview</a>
  &nbsp;|&nbsp;
  <a href="./01-what-is-a-boundary.md">What Is a Boundary ▶</a>
</p>
