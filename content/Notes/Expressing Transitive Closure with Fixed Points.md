---
tags:
  - Note
---
202504101904

Tags : [[Finite Model Theory]]
# Expressing Transitive Closure with Fixed Points
---
Consider a binary relation $R$ on $A$, we will construct $\bar{R}$ which is the transitive closure of $R$.

We know that $R$ is a subset of $A^2$, so we define an inductive operator on $2^{A^2}$, whose least fixed point will be the  transitive closure of $R$.

$$
f(S) = R \cup S \cup \{ (a, b) \mid \exists c\in A, (a, c)\in S, (c, b)\in R\}
$$

If we start with $S_{0} = \emptyset$ we get
- $S_{0} = \emptyset$
- $S_{1} = R$
- $S_{2} = R \cup \{ (a, b) \mid (a, b) \text{ is in the 2 step closure of }R  \}$
- $S_{3} = R \cup \{ (a, b) \mid (a, b) \text{ is in the 3 step closure of }R  \}$
- ...
- $S_{\infty} = \bar{R}$

Existence of such an $S_{\infty}$ is given by [[Knaster-Tarski Theorem]].

---
# References
