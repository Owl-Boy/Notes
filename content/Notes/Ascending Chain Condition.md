---
tags:
  - Note
---
202507061507

Tags : [[Ring Theory]], [[Module Theory]]
# Ascending Chain Condition
---
>[!theorem]
>Let $R$ be a commutative ring, and let $M$  be an $R$-module, then the following are equivalent.
>- $M$ is [[Noetherian Modules|Noetherian]]
>- Every ascending chain of submodules of $M$ stabilizes, this is called the **Ascending Chain Condition**
>- Every nonemtpy family  of sub-modules of $M$ hsa a maximal element wrt inclusion.

2 $\Rightarrow$ 3 is trivial.
for 1 $\Rightarrow$ 2, consider the following ascending chain of sub-modules of $M$:
$$
N_{1} \subseteq N_{2} \subseteq N_{3} \subseteq \dots
$$
Let $N=\bigcup_{i}N_{i}$ and set $N = \langle n_{1},n_{2}\dots n_{k}\rangle$. We know that each $n_{i}\in N_{j}$ for some $j$. Pick the largest such $j$ so we have $N_{j}$ contains all generators of $N$, thus $N_{j}=N$.

For $3\Rightarrow {1}$, let $N$ be a submodules of $M$, then the family of finitely generated submodules of $N$ is non-empty and hence has a maximal element $N'$. If $N'$ is not equal to $N$ then we can add another element to it and we can get a bigger finitely generated sub-modules of $N$. Thus $N$ is finitely generated.

---
# References
- [[Noetherian Modules]]
- [[Noetherian Ring and PIDs]]