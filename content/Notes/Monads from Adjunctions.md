---
tags:
  - Note
---
202507301707

Tags : [[Category Theory]]
# Monads from Adjunctions
---
Given an adjunction $F\dashv U$ between categories $C$ and $D$, consider the information that is present only from the perspective of category $C$. 

- We can construct an endofunctor $UF$
- We have a unit $\eta:1_{C}\Rightarrow UF$
- A whiskered counit which will act as our multiplication $U\epsilon F:UFUF\Rightarrow UF$
And the adjunction laws satsify the commuity commutativity in the following way:
![[Pasted image 20250730173308.png|500]]

The triangles commute by the triangle identities of adjunctions, the square commutes by naturality of vertical natural transfrom.

---
# References
- [[Monads and Comonads]]
- [[Adjunctions]]