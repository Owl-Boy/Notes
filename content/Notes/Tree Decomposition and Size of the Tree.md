---
tags:
  - Example
---

202503312125

tags : [[Finite Model Theory]]

#  Tree Decomposition and Vertex Degree
---
>[!theorem]
>Every non-empty graph $\cal G$ of tree width at most $k$ has a vertex of degree at most $k$.

Consider a small tree decomposition of $\cal G$

Since each leaf's bag contains a vertex which is only found in the leaf, say vertex $v$, the set of edges incident on $v$ cannot exceed the size of the bag that $v$ is in, hence is at most $k$.

---
>[!theorem]
>Every Graph $\mathcal G=(V, E)$ of tree width at most $k$ has at most $k \cdot |V|$ edges.

The proof is again by induction on the size of the graph, one can apply the previous theorem on a vertex, then delete that vertex and keep applying the theorem.

---
# Related
