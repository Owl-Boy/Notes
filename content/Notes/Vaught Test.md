---
id: Vaught Test
aliases:
  - Vaught Test
tags:
  - Note
---
202602102233

Tags : [[Model Theory]]
# Vaught Test
---
> [!THM] Theorem 
> Let $T$ be a satisfiable theory with no finite models that is $\kappa$-categorical for some infinite cardinal $\kappa \ge |\mathcal L|$. Then $T$ is complete.

Suppose $T$ is not complete. Then there is a sentence $\varphi$ such that $T\not\models \phi$ and $T\not\models \lnot\phi$, then both $T_0= T \cup \{\phi\}$ and $T_1=T\cup\{\lnot\phi\}$ are consistent and hence will have models.

Since $T$ has no finite models, both $T_1$ and $T_0$ only have infinite models.

Then by [[Upward Löwenheim–Skolem Theorem]] and [[Downward Löwenheim–Skolem Theorem]]here both have models of size $\kappa$, but $T$ is $\kappa$-categorical, hence we have a contradiction.

---
# References
- [[ACFp is kappa categorical for uncountable kappa]]
- [[Theory of torsion-free divisible Abelian Groups is kappa categorical for uncountable kappa]] 
- [[Upward Löwenheim–Skolem Theorem]]
- [[Downward Löwenheim–Skolem Theorem]]
