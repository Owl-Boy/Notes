---
tags:
  - Note
  - Incomplete
---
202501081601

Tags : [[Logic]]
# Connectivity is not FO Definable
---
>[!theorem] Connectivity of arbitrary graphs is not FO definable

Assume connectivity is definable using a sentence $\Phi$ over vocabulary $\sigma = \{ E \}$. Then expand the vocabulary with 2 constant symbol $c_{1}$ and $c_{2}$, and consider the following formulas
$$
\Psi_{n} = \lnot(\exists x_{1}\dots x_{n}[E(c_{1}, x_{1}) \land E(x_{1},x_{2})\dots E(x_{n},c_{2})])
$$
This formula states that there is no path of length $n+1$ between $c_{1}$ and $c_{2}$ and consider the following theory:
$$
T= \{ \Psi_{n} \}_{n\in \mathbb{N}} \cup \{ c_{1} \neq c_{2},  \lnot E(c_{1}, c_{2})\} \cup \{ \Phi \}
$$
Given any finite subset of the theory, it is clear that it will have a model for it (Just a line graph would work), so by *compactness* we can see that the theory will be consistent, which will imply there will be a model for but, but that means $c_{1}$ and $c_{2}$ are consistent but there is no path of any length between them.
 
---
# References
