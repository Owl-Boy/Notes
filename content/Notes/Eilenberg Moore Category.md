---
tags:
  - Note
---
202508130108

Tags : [[Category Theory]]
# Eilenberg Moore Category
---
Let $C$ be a category with a monad $(T, \eta,\mu)$, The **Eilenberg Moore Category** for $T$ or the category of **$T$-algebras** is the category  $C^T$ whose:
- Objects are pairs $(A\in C,a:TA\to A)$ so that the following diagrams commute in $C$
  ![[Pasted image 20250813014816.png|400]]
- morphisms $f:(A, a)\to (B,b)$ are $T$-algebra homomorphisms: maps $f:A\to B$ in $C$ so that the following square commutes.
  ![[Pasted image 20250813014948.png|150]]

---
# References
- [[Monads and Comonads]]
- [[Affine Spaces as Monads]]
- [[Examples of Eilenberg Moore Categories]]
