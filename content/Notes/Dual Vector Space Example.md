---
tags:
  - Example
---

202412042314

tags : [[Category Theory]]

#  Dual Vector Space Example
---
A finite dimensional vector space $V$ over a field $R$, consider its *Linear Dual*, the vector space $V^*=\text{Hom}(V, R)$. Since these vector spaces have the same dimensions, they are isomorphism, to prove that, one can pick a bases for $V= \{ e_{1}\dots e_{n} \}$ and for $V^*= \{ e_{1}^*\dots e_{n}^* \}$ where $e_{i}^*$ sends $e_{i}$ to $1$ and every other bases vector to $0$.

Now consider the similar construction of the dual of the dual vector space $V^{**}$.  We know that $V^*\cong V^{* *}$ and that $V\cong V^{*}$, this lets us derive $V\cong V^{* *}$. Which can be proved using the composition of bijection of the bases. But there is a simpler construction. Given $v\in V$, consider the map $ev: f \mapsto f(v) :: V^* \to R$. This gives a bijection between an element in $V$ and an element in $V^{* *}$ without requiring us to make an "unnatural" choice of bases. This is related to the fact that the functor $ev$ is naturally isomorphic to the identity endomorphism.

---
# Related
[[Natural Transformation]]