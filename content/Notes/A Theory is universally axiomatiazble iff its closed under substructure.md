---
id: A Theory is universally axiomatiazble iff its closed under substructure
aliases:
  - A Theory is universally axiomatiazble iff its closed under substructure
tags:
  - Note
---
202602151523

Tags : [[Model Theory]]
# A Theory is universally axiomatiazble iff its closed under substructure
---
> [!THM]
> An $L$-theory $T$ is universally axiomatizable iff whenever $M\models T$ and $N$ is a substructure of $M$, then $N\models T$.

Suppose $\mathcal N \subseteq \mathcal M$, then for any quantifier free formula $\phi(\bar v)$ which is quantifier free we have $\mathcal N\models \phi(\bar a)$ iff $\mathcal M\models\phi(\bar a)$.

Then we have the right to left direction trivially.

**Claim**: $T\cup\text{Diag}(\mathcal N)$ is satisfiable.

If not, there is a finite subset $\Delta$ such that $T\cup\Delta$ is not satisfiable. We can take the conjunction of formulas in $\Delta$ and which can be written as $\exists\bar c\bigwedge \phi_i(\bar c)$.

Now we get that $T\models \forall \bar c \bigvee\lnot\phi_i(\bar c)$. But the latter formula is unviersal, so it contradicts $\mathcal N\models \Gamma$

---
# References
- [[Diagram]]
