---
tags:
  - Note
  - Incomplete
---
202502132002

Tags : [[Finite Model Theory]]
# FO(All)
---
Let $\cal P$ be a collection of numerical predicates. 

We define $\text{FO}(\mathcal P)$ as an extension of $\text{FO}$ with atomic formulas of the form $P(x_{1}\dots x_{n})$ for an $n$-ary $P$ in $\cal P$. To define the semantics of this, we order the universe using a total order $\leq$. Then $\mathfrak{A} \vDash P(a_{i_{1}}\dots a_{i_{n}})$ is $(i_{1}\dots i_{n})\in P$.

>[!example] Even
>Let $P_{2} = \{ n | n \equiv 0 \mod 2, n\in \mathbb{N} \}$. consist of even numbers, then the query $\text{EVEN}$ is expressed in $\text{FO}(\{ <, P_{2} \})$ as 
>$$
>\forall x(\forall y(y \leq x) \to P_{2}(x))
>$$  

>[!theorem]
>We define $\text{FO(All)}$ where $\text{All}$ stands for the family of all numerical predicates.

---
# References
