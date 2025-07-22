---
tags:
  - Note
---
202507072307

Tags : [[Category Theory]]
# Two Variable Adjunction
---
>[!definition]
>A triple of bifunctors
>$$
>A \times B \xrightarrow F C,\quad A^\text{op}\times C \xrightarrow G B,\quad B^\text{op}\times C \xrightarrow H A
>$$
>Equipped with a natural isomorphism
>$$
>C(F(a,b), c)\cong B(b, G(a, c))\cong A(a, H(b, c))
>$$
>defines a **two-variable adjunction**.

In particular when $F:C\times C \to C$ defines some monoidal product, its pointwise defined right adjoints are called its **left** and **right closures** respectively. When these are isomorphic the bifunctor is called [[Monoidal Closed Category|closed]].

---
# References
- [[Cartesian Closed Category]]
- [[Adjunction of Bifunctors]]
- [[Adjunctions]]
- [[Monoidal Closed Category]]