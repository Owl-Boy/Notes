---
tags:
  - Note
---
202507072307

Tags : [[Category Theory]]
# Adjunction of Bifunctors
---
>[!theorem]
>Suppose $F:A \times B \to C$ is a bifunctor such that for each $a:A$ the induced functor $F(a,-):B\to C$ admits a right adjoint $G_{a}:C\to B$. Then:
>- The right adjoints assemnle into a unique bifunctor $G:A^\text{op}\times C \to B$ so that the isomorphism 
>  $$
>  C(F(a,b),c)\cong B(b,G(a, c))
>  $$
>  is natural in all 3 variables
>  
>If $b:B$, the induced functor $F(-,b):A\to C$ admits a right adjoint $H_{b}:C\to A$ then,
>- There is a unique bifunctor $H:B^\text{op}\to C$ defined so that $H(b,c)=H_{b}(c)$ and the isomorphisms
>  $$
>  C(F(a, b),c)\cong B(b,G(a, c)) \cong A(a, H(b, c))
>  $$
>  are natural in all 3 variables.
>- For each $c$, the functors $G(- , c):A^\text{op}\to B$ and $H(-,c):B^\text{op}\to A$ are mutual right adjoints.

---
# References
- [[Adjunctions]]
- [[Mutual Left and Right Adjunctions]]
- [[Unique construction of Adjunction]]
- [[Two Variable Adjunction]]