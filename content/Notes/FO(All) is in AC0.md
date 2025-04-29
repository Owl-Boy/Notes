---
tags:
  - Note
  - Incomplete
---
202502131802

Tags : [[Finite Model Theory]], [[Complexity Theory]]
# $\text{FO(All)}$ is in $\text{AC}^0$
---

>[!theorem]
>Let $\mathcal{C}$ be the class of structures definable by an $\text{FO(All)}$ sentence. Then $\cal C$ is nonuniform $\text{AC}^0$. Furthermore for every $\text{FO(All)}$ sentence $\Phi$, there is a family of circuits of depth $O(\| \Phi \|)$ accepting $\{ \mathfrak A | \mathfrak A \vDash \Phi \}$.

If $k\neq \| \mathfrak A \|$ for any structure that satisfies $\Phi$ $C_{k}$ returns $\bot$. 
For all other cases, we replace $\exists x \varphi(x, \vec{y})$ and $\forall \varphi(x, \vec{y})$ with
$$
\bigvee_{c=0}^{n-1}\varphi(c, \vec{y}) \quad \text{and}\quad
\bigwedge_{c=0}^{n-1}\varphi(c,\vec{y})
$$
respectively. The number of characters used to write the formula have not changed. We now build a circuit for this modified formula, the relation symbols can be constructed based on the encoding of the relation trivially. 

This construction adds a depth of at most $3$ for each connective used and of at most 2 for each atomic formula, so the depth is clearly in $O(\| \Phi \|)$.

If the quantifier depth is $k$ then the size of the circuit is $O(n^k)$. So it is polynomial.

>[!theorem] Corollary
>The [[Data Complexity of a Logic|Data Complexity]] of $\text{FO(All)}$ is in [[AC0|Nonuniform]] $\text{AC}^0$.

---
# References
[[FO(All)]]