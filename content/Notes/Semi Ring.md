---
tags:
  - Note
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
>with axioms the following axioms:
>- $\langle S, +, 0 \rangle$ forms a commutative monoid
>- $\langle S, \cdot, 1, \rangle$ forms a monoid
>- multiplication distributes over addition, both left and right.
>- $\forall a, \quad a \cdot 0 = 0 \cdot a = 0$

>[!example]
>- $\mathbb{N}, \mathbb{R}, \mathbb{Z}$ under standard $+$ and $\times$.
>- $\langle \mathbb{Z} \cup \{ \infty \}, \min, +, \infty, 0 \rangle$, this is called a min-tropical algebra.
>- $\langle \{ \top,\bot \}, \land, \lor,\top, \bot \rangle$, this is also called the boolean semi ring.

---
# References
[[Polynomial and matrices over semi rings form semi rings]]