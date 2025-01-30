---
tags:
  - Note
---
202501201501

Tags : [[Weighted Automata and Transducers]]
# Reachable Vectors
---
As depicted in the [[Algorithm for Finding the Weight of a Word#Matrix Implementation]], we can see that each word $w=a_{1}a_{2}\dots a_{n}$ can be represented as the vector $I \cdot \mu_{a_{1}} \cdot \mu_{a_{2}}\dots \mu_{a_{n}}$.

We call the set of all vectors that can be produced in this manner as **Reachable Vectors**.

If the semi-ring of the weighted automata is a sub-semi-ring of a field, then we can think of the above set of **Reachable Vectors** sitting in a vector space, called the **Reachable Subspace**. This, in general will be a strict super-set of the set of **Reachable Vectors**.

The basis for the **Reachable Subspace** is called the **Reachable Basis** and is useful in many algorithms.

---
# References
