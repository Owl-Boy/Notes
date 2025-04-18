---
tags:
  - Example
---

202503311355

tags : [[Finite Model Theory]]

#  Tree Decomposition Lemma 1
---
>[!lemma]
>Let $(\mathcal T, (B_{t})_{t\in T})$ be a tree decomposition of the graph $\cal G=(V, E)$. Then for every edge $(t, u)$ of $\cal T$.
>$$
>B_{u} \cap B_{t}
>$$
>separates $B(T \setminus T_{u})$ from $B(T_{u})$ in $\cal G$

Let $V_{t} = B(T \setminus T_{u})$ and $V_{u}=B(T_{u})$, let $v_{1} \dots v_n$ be a path in $\cal G$ from $V_{t}$ to $V_{u}$, then we need to show that there is an $i\in [1..n]$ such that $v_{i}\in V_{u}\cap V_{t}$, or ($v_{i}\in V_{u}$ and $v_{i+1}\in V_{t}$).

Suppose $v_{i}\in V_{u} \cap V_{t}$, then $B^{-1}(v_{i})$ intersects with both $T_{u}$ and $T \setminus T_{u}$, and since the graph is connected, it must pass through the the $(u, t)$ edge.

If $v_{i}\in V_{u}$ and $v_{i+1}\in V_{t}$, then $B^{-1}(v_{i})$ intersects with $T_{u}$ and $B^{-1}(v_{i+1})$ intersects with $T\setminus T_{u}$, but since $v_{i}$ and $v_{i+1}$ are adjacent in the graph, there must be a vertex  $t\in \cal T$ such that $v_{i},v_{i+1} \in B_{t}$. Which means wither $B^{-1}(v_{i})$ or $B^{-1}(v_{i+1})$ intersects with both sides of the tree, now the argument for the previous case works. 

---
# Related
