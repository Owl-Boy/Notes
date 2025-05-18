---
tags:
  - Note
  - Incomplete
---
202505141905

Tags : [[Homotopy Type Theory]]
# Examples of Sets in Type Theory
---
>[!example]
>The type $\mathbf{1}$ is a set. From [[Higher Groupoid Structure of Unit Type]] we get that for all $x,y : \mathbf{1}$ the type $x=y \simeq \mathbf{1}$.

>[!example]
>The type $\mathbf{0}$ is a set, as for any $x,y$ we can deduce whatever we want.

>[!example]
>The type $\mathbb{N}$ is also a set, since all equality types are either equivalent to $\mathbf{0}$ or $\mathbf{1}$, in both cases, any 2 elements of the type are equal.

>[!example]
>If $A$ and $B$ are sets, then $A \times B$ will also be a set.

>[!example]
>If $A$ is *any type* and $B(x)$ is a set for each $x:A$ then the type $\prod_{(x:A)}B(x)$ is a set.
>
>Suppose $f,g: \prod_{(x:A)}B(x)$ and $p,q:f=g$, then we have
>$$
>p=\text{funext}(x \mapsto \text{happly}(p, x))\quad \text{and} \quad q=\text{funext}(x \mapsto \text{happly}(q, x))
>$$
>And for any $x$ we have $f(x)=g(x)$ by $\text{happly}(p,x)$ and $\text{happly}(q, x)$, hence by $\text{ap}_{\text{funext}}$ we have $p=q$.



$$
>$$

---
# References
