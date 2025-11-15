---
tags:
  - Note
  - Incomplete
---
202510041910

Tags : [[Parameterized Algorithms]]
# Kernelization Algorithm for Edge Clique Cover
---
The **Edge Clique Cover** problems asks, given a graph $G$ and a natural number $k$, is it possible to cover the edges of $G$ with at most $k$ cliques.

For solving this problem, we define:
>[!definition]
>A **neighbourhood** of a vertex $v$ in a graph $G$, also written as $N(v)$ is the set of vertices adjacent to $v$. The **closed neighbourhood** of a vertex $v$ is $N[v]=v:N(v)$.

With this defined, we have the following reductions:
- Remove isolated vertices $v$ \[$(G, k)\to(G-v,k)$]
- If there is an isolated edge $uv$ delete it and decrement $k$ by $1$ \[$(G,k)\to(G-uv,k-1)$]
- If there are 2 vertices $u,v$ such that $N[u]=N[v]$ then merge them \[$(G, k)\to(G-v,k)$]
Now we need to show that this forms a kernel, that is the number of vertices are a function of $k$.

If this is a yes-instance, Let $C_{1}\dots C_{k}$ be the cliques used to cover the graph. There is no two vertices that are in exactly the same subset of cliques, otherwise rule $3$ is applicable. Hence we are done.

---
# References
- [[Kernelization]]