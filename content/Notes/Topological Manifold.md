---
tags:
  - Note
---
202508071808

Tags : [[Manifolds]], [[Topology]]
# Manifold
---
A **manifold** is a topological space that locally resembles a Euclidean Space near each point.

>[!definition]
>Let $X$ be a [[Topological Spaces|topological space]]. A **co-ordinate chart** on $X$ is the data of:
>- An open set $U \subseteq X$.
>- An open set $\tilde{U} \subseteq R^n$
>- A homeomorphism 
>  $$
>  f : U \to \tilde{U}
>  $$

**Co-ordinate charts** help us define local transformation 

>[!definition]
>Fixing an natural number $n$ an $n$**-dimensional topological manifold** is a topological space $X$ such that $X$ is [[Second Countability|second countable]] and [[Hausdorff Property|hausdorff]] and for any point if for any point $x\in X$ we can find a coordinate chart
>$$
>f:U\to \tilde{U}
>$$
>with $x \in U$. The set of all (possibly infinite) co-ordinate charts is called an **atlas**.

The [[Unit Circle is a Manifold]]

>[!definition]
>A **topological manifold** is called **smooth** iff for any 2 charts in the atlas. The transition function:
>$$
>\phi_{ij}:f_{j}(U_{i} \cap U_{j}) \xrightarrow \sim f_{i}(U_{i}\cap U_{j})
>$$
>is a [[Smooth Function]].

---
# References
- [[Topological Spaces]]
- [[Hausdorff Property]]
- [[Second Countability]]