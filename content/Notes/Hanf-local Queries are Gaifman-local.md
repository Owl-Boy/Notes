---
tags:
  - Note
  - Incomplete
---
202501300001

Tags : [[Finite Model Theory]]
# Hanf-local Queries are Gaifman-local
---
>[!theorem] 
>If $Q$ is a [[Hanf-Locality|Hanf local]] non-boolean query, then $Q$ is [[Gaifman-Locality|Gaifman local]], and $\text{lr}(Q) \leq 3 \cdot \text{hlr}(Q)+1$.

Using [[FO Queries are Hanf Local]], Consider 2 copies of $\mathfrak A$ which have $\text{hlr}(Q)=d$ and $\vec{a}_{1} \approx_{3d+1} \vec{a}_{2}$. But since $\mathfrak A \leftrightarrows_{d} \mathfrak A$ we have $(\mathfrak A, \vec{a}_{1}) \leftrightarrows (\mathfrak A, \vec{a}_{2})$ because of [[Local Equivalence Lemma]].

So $a_{1} \in Q(\mathfrak A) \iff a_{2} \in Q(\mathfrak A)$ which shows that $\text{lr}(Q) \leq 3d+1$.

Another corollary for this is, if $Q$ is defined by a $\text{FO}[k]$ formula then 
$$
\text{lr}(Q) \leq \frac{3^{k+1} -1}{2}
$$


---
# References
