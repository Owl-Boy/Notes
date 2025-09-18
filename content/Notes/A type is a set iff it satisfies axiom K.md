---
tags:
  - Note
---
202508280008

Tags : [[Homotopy Type Theory]]
# A type is a set iff it satisfies axiom K
---
>[!theorem]
>A type $X$ is a [[Sets in Type Theory|set]] if and only if it satisfies [[Axiom K]].

We have that Axiom $K$ holds for a set $X$ if it is a set. For the other direction, we need to show that if a type $X$ satisfies axiom K, then it is a set. So consider any $x, y:X$ and $p,q:x=y$, if we path induct on $q$, then we need to show that $p=\text{refl}_{x}$ which is precisely axiom K.

---
# References
- [[Axiom K]]
