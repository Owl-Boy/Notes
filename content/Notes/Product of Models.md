---
id: Product of Models
aliases:
  - Product of Models
tags:
  - Note
---
202601172022

Tags : [[Model Theory]] 
# Product of Models
---
Given a set $I$ which indexes a collection of models $\{\mathcal M_i\}_{i\in I}$ we can define the product model $\mathcal M = \prod_{i:I} \mathcal M_i$ as follows:
- The underlying universe is defined as $M = \prod_{i:I}M_i$.
- A constant symbol $c$ is interpreted as the function $i\mapsto c^{\mathcal M_i}$
- A function symbol $f$ of arity $n$, whose input will an element $a:M^n$, which can be thought of as $\prod_{i:I} a_i$ where $a_i:M^n$. Then the function $f^\mathcal M$ will send $a$ to $i\mapsto f^{\mathcal M_i}(a_i)$.
- A relation symbol $r$ of arity $n$, whose input is $a:M^n$, wich can be thought of in a similar manner as above contains $a$ iff $r^{\mathcal M_i}(a_i)$ holds for all $i$.

The projection maps $\pi_i : \mathcal M \to\mathcal M_i$, which are defined in the obvious way are [[Homomorphism of Models]] and this construction satisfies the [[Universal Property (Riehl)|Universal Property]] of [[Products and Coporducts|products]].

This model intuitively captures the sentences that are true in all component models.

---
# References
- [[Semantics of First Order Logic]]
- [[Homomorphism of Models]]
- [[Products and Coporducts]]
- [[Universal Property (Riehl)]]
