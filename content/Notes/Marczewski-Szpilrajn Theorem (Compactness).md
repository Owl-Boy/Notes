---
id: Marczewski-Szpilrajn Theorem (Compactness)
aliases:
  - Marczewski-Szpilrajn Theorem
tags:
  - Note
  - Incomplete
---
202602151719

Tags : [[Model Theory]] [[Order Theory]]
# Marczewski-Szpilrajn Theorem
---
> [!THM]
> Any Partial order can be extened to a linear ordre.

Consider the theory of partial orders $\text{PO}$:
$$
\begin{aligned}
\forall x&, x \le x\\
\forall x\ y\ z&, x\le y \land y\le z\Rightarrow x\le z\\
\forall x\ y&, x\le y \land y\le x \Rightarrow x=y
\end{aligned}
$$

And the theory of total orders $\text{TO}$ include the following axiom

$$
\forall x\ y, x\le y \lor y\le x
$$

then consider a model $(X, \preceq)\models \text{PO}$ 

Let $T_X= \text{TO}\cup\text{Diag}(X,\preceq)$. **Claim**: This is satisfiable.

By compactness, we only need to check for finite subsets, we will check for $\text{TO}$ union finite subsets of $\text{Diag}(X, \preceq)$, let $D$ be such a set.

> [!LEM]
> Any finite partial order can be linearized. (Keep picking a maximal element)

Thus we have that for any such $D$, we will take the subset of $X$ whose corresponding constants are in $D$ and then linearize it using the lemma. Thus any $D$ has a model.

Thus $T_X$ has a model $M$ that agrees with $X$. But since [[A Theory is universally axiomatiazble iff its closed under substructure]], we can take a subset of $M$ such that $X$ injects into it, and we get a linearization of $X$.

---
# References
- [[Compactness Theorem]]
- [[A Theory is universally axiomatiazble iff its closed under substructure]]
