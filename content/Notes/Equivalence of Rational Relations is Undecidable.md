---
tags:
  - Note
---
202504191504

Tags : [[Weighted Automata and Transducers]]
# Equivalence of Rational Relations is Undecidable
---
The proof will be a reduction from [[Post Correspondence Problem|PCP]].

First Consider the following relations $\Sigma_{1}^* \times \Sigma_{2}^*$.
For the other relation, let $F,G:\Sigma_{1}^* \to \Sigma_{2}^*$ be 2 monoid homomorphisms.

Consider the following relations:
- $R_{F}= (w, \Sigma_{2}^* \setminus \{ F(w) \})$
- $R_{G} = (w, \Sigma_{2}^* \setminus \{ G(w) \})$
- $R = R_{F} \cup R_{G}$

This language will be exactly $\Sigma_{1}^* \times \Sigma_{2}^*$ for there is no word $w$ such that $F(w) = G(w)$.

Note that the languages $R_{F}$ and $R_{G}$ are easy to construct as a rational relation, by the automata construction.

---
# References
