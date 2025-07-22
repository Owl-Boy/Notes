---
tags:
  - Example
---

202506131705

tags : [[Homotopy Type Theory]]

#  Path Connected Component Functor
---
One can construct the path-connected functor as follows:
- First consider the functor $\text{Path}(X) := I \to X$, which is the set of paths in a space. This is a set.
- Also consider the functor $\text{Point}(X) := * \to X$, which should be naturally isomorphic to the forgetful functor, so it just gives the collection of points in the space as a set.
- One can evaluate a path at the starting and ending points, which give functors form $\text{Path}(X)$ to $\text{Point}(X)$.
- This gives us a functor $P:\text{Top} \to\text{Set}^{\bullet\rightrightarrows\bullet}$. 
- Given a diagram of the shape $\bullet \rightrightarrows\bullet$ in set, it represents the set of points in a topological space, and in its colimit is takes the set of points in a topological space, and quotients them together if there is a path connecting them. Hence composing teh colimit functor with $P$ gives the path connected component functor.

---
# Related
- [[Choosing Limits of diagrams in Functorial]]
- [[Top is Complete and Cocomplete]]
- [[Path Connectedness]]