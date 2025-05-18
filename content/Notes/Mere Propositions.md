---
tags:
  - Note
  - Incomplete
---
202505171805

Tags : [[Homotopy Type Theory]]
# Mere Propositions
---
The idea of propositions as types leads to outcomes like [[Type Theoretic Axiom of Choice]] being provable and that [[Double Negation Does Not Cancel]]. Both of these happen because any logical operation must also respect the extra $\infty$-groupoid structures. 

Hence, we can try to get a more convensional logic on types that have a trivial $\infty$-groupoid structure. This leads us to:
>[!definition]
>A type $P$ is a **Mere Proposition** if for all $x,y:P$ we have $x=y$.

To specify that a type is a **mere proposition** we can also define the following
$$
\text{is-Prop}(P) :\equiv \prod_{x, y:P}(x=y).
$$
We have some simple lemmas for them:
>[!lemma]
>If $P$ is a **mere proposition** and $x_{0}:P$  then $P \simeq \mathbf{1}$

>[!lemma]
>If $P$ and $Q$ are **mere propositions** such that $P\to Q$ and $Q \to P$ then $P\simeq Q$.

---
# References
