# Chapter 5 — Architectural Units

## Purpose of This Chapter

This chapter introduces architectural units as the structural elements that give architecture shape beyond layers. While layers define zones of responsibility and closed layers enforce boundaries, architectural units define how responsibility is packaged, named, and reasoned about within and across those layers.

Architectural units exist to make architecture explicit, navigable, and enforceable at a scale that aligns with how systems are built and evolved. They provide a way to talk precisely about parts of the system, to define contracts intentionally, and to prevent architectural decisions from dissolving into implementation detail.

---

## What This Chapter Covers

- what an architectural unit is in architectural terms
- how architectural units differ from projects, services, and components
- why architectural units exist independently of layers
- how units enable clear contracts and boundary crossings
- common ways architectural units are misused or diluted

---

## What This Chapter Does Not Cover

- specific project or repository layouts
- language or framework constructs
- dependency injection configuration
- build or deployment mechanics
- code-level implementation patterns

---

## How This Chapter Builds on Closed Layers

Closed layers establish where access is restricted and why enforcement matters. Architectural units operate within that context by defining the concrete units of responsibility that participate in those layers. They give architects a vocabulary for expressing intent, ownership, and interaction without collapsing back into code-level concerns.

Readers should approach this chapter with the understanding that architectural units are not a replacement for layers or boundaries. They are the means by which those concepts become precise and scalable in real systems.

---

## What Comes After This

With architectural units defined, the next chapters introduce contracts, boundary crossings, and dispatch mechanisms that govern how units interact without violating closed layers. Together, these concepts complete the architectural model and make enforcement possible without relying on convention.

---

<p align="center">
  <a href="../chapter-04-closed-layers/README.md">◀ Chapter 4 Overview</a>
  &nbsp;|&nbsp;
  <a href="./01-what-are-architectural-units.md">What Architectural Units Are ▶</a>
</p>
