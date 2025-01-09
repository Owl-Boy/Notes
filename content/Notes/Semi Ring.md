---
tags:
  - Note
  - Incomplete
---
202501092301

Tags : [[Weighted Automata and Transducers]]
# Semi Ring
---
A *Semi Ring* is a set equipped with 2 binary operators, generally known as addition and multiplication which make monoid with the set, and the multiplication operator respects the addition operator.

>[!definition]
>A *semi ring* is defined by the followin 5-tuple
>$$
>\langle S, +, \cdot, 0, 1 \rangle
>$$ 
>
>with axioms that state that 
>- Both operators are associative
>- multiplication distributes over addition
>- $1$ is identity for $\cdot$
>- $0$ is identity for $+$ and annihilator for $\cdot$

>[!example]
>- $\mathbb{N}, \mathbb{R}, \mathbb{Z}$ under standard $+$ and $\times$.
>- $\langle \mathbb{Z} \cup \{ \infty \}, \min, +, \infty, 0 \rangle$, this is called a min-tropical algebra.

---
# References
[[Polynomial and matrices over semi rings form semi rings]]