---
tags:
  - Note
  - Incomplete
---
202505051305

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Unit Type
---
>[!theorem]
>For any $x, y: \mathbb1$ we have $(x=y)\simeq \mathbb 1$.

The function $f:x=y \to \mathbb 1$ is easy to define. Also to define a function of type $g:\mathbb {1} \to x=y$ we only need to define it for the case when $x\equiv y$, hence $\star \mapsto \text{refl}_{*}$ works.

We now need to show that these are inverses. First consider an element $u:\mathbb 1$, assume $u=\star$. $f(g(u))=u$

For the reverse, given $p:x=y$, we assume by path induction that $p \equiv\text{refl}_{x}$, hence the composition takes $p$ to $p$

---
# References
