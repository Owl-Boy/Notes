---
id: Dedekind Reals (HoTT)
aliases:
  - Dedekind Reals
tags:
  - Note
  - Incomplete
---
202602172115

Tags : [[Homotopy Type Theory]]
# Dedekind Reals
---
We use the 2-sided dedekind cuts because the symmetry makes the construction more elegant.

A dedekind cut of the ration numbers $\mathbb Q$ consists of a pair $(L, U)$ which are subsets of $\mathbb Q$ given by a functions $L,U:\mathbb Q\to \mathbb P$ such that:
- *inhabited*: $\exists (q:\mathbb Q). L(q)$ and $\exists (r:\mathbb Q).U(r)$,
- *rounded*: for all $q, r:\mathbb Q$
  - $L(q)\Leftrightarrow \exists (r:\mathbb Q).(q < r) \land L(r)$ and
  - $U(r)\Leftrightarrow \exists (q:\mathbb Q).(q < r) \land U(q)$
- *disjoint*: $\forall (q:\mathbb Q).\lnot(L(q)\land U(q))$

we define $\text{isCut}$ as the conjunction of the above and we define the set of dedekind real numbers as follows:
$$
\mathbb R_d :\equiv \{(L, U): (\mathbb Q \to \mathbb P) \times (\mathbb Q \to \mathbb P)\mid \text{isCut}(L, U)\}
$$

Since each of the given conditions are [[Mere Propositions]] we get that $\mathbb R$ is a set.

There is an embedding of rationals into the dedekind reals as follows:
$$
\begin{matrix}
L_q :\equiv \{r:\mathbb Q \mid r < q\}&\text{and}&U_q:\equiv\{r:\mathbb Q\mid q<r\}
\end{matrix}
$$

---
# References
- [[Sets in Type Theory]]
- [[Reals are a Field]]
