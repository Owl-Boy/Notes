---
id: Homomorphism of Models
aliases:
  - Homomorphism of Models
tags:
  - Note
---
202601171959

Tags : [[Model Theory]]
# Homomorphism of Models
---
On fixing a language $L$, given 2 $L$-models $\cal M, N$, we define a **model homomorphism** $\hat h:\cal M\to N$ as:

> [!DEF] Definition
> The homomorphism $\hat h$ carries the following data:
> - $h:M\to N$
> - For any constant symbol $c$ we have $h(c^{\cal M}) = c^{\cal N}$
> - For any function symbol $f^{(n)}$ we have $h(f^{\cal M}(\bar a))=f^{\cal N}(h(\bar a))$
> - For any relation symbol $r^{(n)}$ we have $r^{\cal M}(\bar a)\Rightarrow r^{\cal N}(h(\bar a))$

This does define a [[Category]].

Such a morphism is called **Strict** if for any relation symbol $r^{(n)}$, and for any witness $\bar a \in h(M)$ such that $r^{\mathcal N}(\bar a)$, there is a witness $\bar b\in M$ such that $\bar b \in r^{\cal M}$.

This also defines a category.

---
# References
- [[Semantics of First Order Logic]]
