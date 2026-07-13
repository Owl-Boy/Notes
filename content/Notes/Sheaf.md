---
id: Sheaf
aliases: []
tags:
  - Note
  - Incomplete
---

202607131523

Tags : [[Topos Theory]]

# Sheaf

A *Sheaf* is like a [[Topos of Bundles|bundle]] with a topological structure on it.

Let $I$ be a topological space, and $p: A \to I$ be a local homeomorphism. We denote the category of sheaves over $I$ with $\text{Top}(I)$ which has such pairs $(A, p)$ as its objects, and as arrows, open maps $k : (A, p) -> (B, q)$ such that $p = k \triangleright q$.

$\text{Top}(I)$ is again a sheaf with $(I, \text{id}_I)$ being the terminal object.

The sub-object classier is a sheaf defined over the set $\mathcal{O}(I)$ where we the fibre over $i$ is given by quotienting the frame of open sets with the prime filter of open sets that contain $i$.

Given an open set $U$ and an element $i$, the prime filter over $i$ gives us the following:
- If $i \in U$ then we get $[U]_i = [I]_i$ and vice versa.
- $[I]_i = \mathcal{O}(I)_i$
- If $i$ is separated from $U$ then we get that $[U]_i = [\emptset]_i$

Arrows from  the terminal object are considered as continuous sections. To see that that looks like, consider an open set $U$. and we then construct the function $S_U$ such that it maps $i$ to $(i, [U]_i)$. This is a continuous global section. Then consider any section $s$, and the subset $U = {i \mid s(i) = [I]_i}$, we will get that $s = S_U$.

Given $k :(A, p) \hookrightarrow (B, q)$ we define it's character $xi_k$ as a map from $B -> \hat {I}$, where $x$ is sent to the germ of $q(A\cap S)$ at $q(x)$, where $S$ is an open subset of $B$ where the map is a homoemorphism.

There will a lot of constructions with set theoretic and topological interpretations, where we replace the word "set" with "open set".

# References

- [[Topos of Bundles]]
