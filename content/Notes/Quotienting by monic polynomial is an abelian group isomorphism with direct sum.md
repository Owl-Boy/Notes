---
tags:
  - Note
  - Incomplete
---
202505211505

Tags : [[Ring Theory]]
# Quotienting by monic polynomial is an abelian group isomorphism with direct sum
---
>[!lemma]
>Let $R$ be a commutative ring, and let $f:R[x]$ be a monic polynomial of degree $d$. Then the function:
>$$
>\varphi : R[x] \to R^{\oplus d}
>$$
>by sending $g(x)$ to its remainder when divided by $f$ induces an abelian group isomorphism between:
>$$
>\frac{R[x]}{(f(x))} \cong R^{\oplus d}
>$$

To show that this is a homomorphism between abelian groups is trivial. This is also clearly surjective, because for any element in $R^{\oplus d}$, one can find a polynomial of degree d, which must map back to the element.

We also have that this is an injection, because $g(x)$ goes to $0$ iff $g(x)=f(x)q(x)$, that is it belongs to $(f(x))$.


---
# References
