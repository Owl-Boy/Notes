---
tags:
  - Note
---
202511050011

Tags : [[Homotopy Type Theory]]
# Limits and Colimits in the category of sets
---
Since sets are closed under products, the universal property of products show that $\text{Set}$ has finite products. In fact infinite products are also easy:
$$
\left( X \to \prod_{a\text{A}}B(a) \right) \simeq \left( \prod_{a:A} X\to B(a) \right)
$$
given by swapping the arguments. We have that a pullback of function $f:A\to C$ and $g:B\to C$ can be defined as $\sum_{a:A}\sum_{b:B}f(a)=g(b)$. This is a set if $A,B,C$ are and has the correct universal property, therefore the category [[Set is Complete]].

Since $\text{Set}$ is closed under $+$ and set has $\mathbf{0}$, it has all finite coproducts, and since $\sum_{a:A}B(a)$ is a set, whenever $A$ is a set and all $B(a)$ are sets, infinite coproducts are also sets. We also have a way to construct [[Pushouts of n-types]], thus [[Set is Complete and Cocomplete]].

---
# References
- [[Category of Sets (HoTT)]]
- [[Limits and Colimits]]
- [[Limits in the Category of Sets]]
- [[Set is Complete]]