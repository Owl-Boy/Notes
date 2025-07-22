---
tags:
  - Note
---
202507030007

Tags : [[Category Theory]]
# Adjunctions in Posets
---
As discussed in [[Examples of Adjunctions#^1b3d49]], we define a [[Galois Connection]] as an adjunction between 2 partial orders.

Let $F\dashv G$ be a galois connection. Then we get the following fixed point formula:
$$
FGF = F
$$
and
$$
GFG = G
$$
The proof is simple given, the triangle identities give that $F(a)\leq FGF(a) \leq F(a)$ for all $a$. So we are done.

>[!example]
>Consider the Galois Connection direct image-inverse image induced by a function $f$:
>Then we get the following inclusions
>$$
>X \subseteq f^{-1}f(X)\quad\quad\text{and}\quad\quad f(f^{-1}(Y)) \subseteq Y
>$$
>But the following are equalities
>$$
>f(X)=f(f^{-1}(f(X)))\quad\quad\text{and}\quad \quad f^{-1}(f(f^{-1}(Y)))=Y
>$$

---
# References
- [[Adjunctions]]
- [[Unit and Counit as Universal Arrows]]
- [[Galois Connection]]
- [[Examples of Adjunctions]]