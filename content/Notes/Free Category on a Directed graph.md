---
tags:
  - Example
---
202507021707

Tags : [[Category Theory]]
# Free Category on a Directed graph
---
The functor $U:\text{Cat}\to\text{DirGraph}$ admist a let adjoint $F$, defining the free category on a directed graph.

The functor sends a directed graph to a category with the same sets as its objects and a "path" as a morphism.

>[!example]
>The category $\omega$ is free on the directed graph whose vertices are indexed by natural numbers and with successor on edges.

>[!example]
>Let $\mathbb{n+1}$ denote the ordinal category. For each $0\leq i\leq n$, there is an injecitve functor $d^i:\mathbb{n}\to \mathbb{n+1}$ where $i\in \mathbb{n+1}$, where $i$ is the unique object missing from the image. There is also a surjective functor $s^i:\mathbb{n+1}\to \mathbb{n}$. for which $i$ is the unique object with 2 pre-images, then there is sequence of adjoints:
>![[Pasted image 20250702180913.png|250]]


---
# References
- [[Adjunctions]]