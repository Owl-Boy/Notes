---
tags:
  - Note
  - Incomplete
---
202504201604

Tags : [[Weighted Automata and Transducers]]
# Checking if a word is related to $\Sigma_{2}^*$
---
>[!theorem]
>Given a [[Rational, Automatic and Recognizable relations|rational relation]] $R$, checking if for all $w$ we have that $\{ w \}\times \Sigma_{2}^* \subseteq R$ is undecidable.

The proof for this is straightforwards, we can define relations $(w, \overline{F(w)})$ and $(w, \overline{G(w)})$ and consider their union, If for all $w$ we have $\{ w \} \times \Sigma_{2}^* \subseteq R$ then we show that there is no witness to PCP, which is undecidable.

---
>[!theorem]
>Given a *rational relation* $R$, check if there exists a word $w$ such that $\{ w \}\times \Sigma_{2}^* \subseteq R$ in undecidable.

The proof for this is also similar, we construct relations $(w, \overline{F(w)})$ and $(w, G(w))$ for homomorphisms $G$ and $F$, then $\{ w \}\times \Sigma_{2}^* \subseteq R$ iff $F(w)=G(w)$ which becomes a witness for post correspondence problem.

---
# References
