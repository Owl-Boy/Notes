---
tags:
  - Note
  - Incomplete
aliases: []
id: Solving Synchronous Distributed Games
---
202603232024

Tags : [[Concurrency Theory]]

# Solving Synchronous Distributed Games

---

> [!QUESTION] Solving a SDG
> Given an SDG, does there exist a winning strategy?

This problem, is neither [[Recursive and Recursively Eumberable Sets|recursive]] nor co-recursive.

> [!QUESTION] Solving a SDG with finite memory
> Given an SDG, does there exist a finite-memory winning strategy?

This problem is recursive.

> [!QUESTION] Finding a finite memory strategy for an SDA
> Given an SGD, find a finite memory winning strategy

> [!THM] Sufficient condition for undecidability 2
> If the [[Information Pre-Order]] is not a tier-list (contains incomparable elements), then the first 2 problems are undecidable, even when the winning condition is given in [[Linear Temporal Logic|LTL]]. 

> [!THM] Sufficient condition for undecidability 1
> If the [[Information Pre-Order]] is a tier-list (all elements are comparable), then the first 2 questions are decidable. If there does exist a winning strategy, then we can construct a finite memory winning strategy.

---

# References
- [[Synchronous Distributed Games]]
- [[Recursive and Recursively Eumberable Sets]]
- [[Games on Graphs]]
