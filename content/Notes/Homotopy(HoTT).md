---
tags:
  - Note
  - Incomplete
---
202505041105

Tags : [[Homotopy Type Theory]]

# Homotopy
---
>[!definition]
>Given 2 functions $f,g: \prod_{x:A} P(x)$, a **Homotopy** between $f$ and $g$ is the dependent type
>$$
>(f \sim g) :\equiv \prod _{x:A} f(x)=g(x)
>$$

The following lemma states that this is an equivalence relation:
>[!lemma]
>A Homotopy is an equivalence relation, on each dependent function type $\prod_{x:A}P(a)$. That is, we have elements of the following type:
>$$
>\begin{gather}
>\prod_{f:\prod_{x:A}P(x)}(f \sim f)\\
>\prod_{f,g:\prod_{x:A}P(x)}(f \sim g) \to (g \sim f)\\
>\prod_{f,g,h:\prod_{x:A}P(x)}(f \sim g) \to (g \sim h) \to (f \sim h)
>\end{gather}
>$$

The same way we found that functions are functorial, we shall see that homotopies are natural transformations.

For non-dependent functions we get the following:
>[!lemma]
>Suppose $H:f \sim g$ is a homotopy between $f,g:A \to B$ and let $p:x =_{A} y$, then:
>$$
>H(x) \cdot g(p) = f(p) \cdot H(y)
>$$

For the proof, induct of $p$, we get $H(x) \cdot \text{refl}_{g(x)} = \text{refl}_{f(x)} \cdot H(x)$, which are judgementally equal so we are done.

---
# References
