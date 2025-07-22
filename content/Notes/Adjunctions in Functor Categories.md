---
tags:
  - Note
  - Incomplete
---
202507111707

Tags : [[Category Theory]]
# Adjunctions in Functor Categories
---
>[!theorem]
>Given an adjunction:
>![[Pasted image 20250711171209.png|100]]
>post-composition with $F$ and $G$ defines a pair of adjoint functors:
>![[Pasted image 20250711171237.png|100]]
>for any small category $J$, and pre composition with $F$ and $G$ also define an adjunction
>![[Pasted image 20250711171318.png|100]]
>For any locally small category $E$.

The sexy proof for this one is to realise that adjunctions can be written down internally in a 2-category as we can express natural transformations inside them. Then we use an idea analagous the the fact that Functors preserve commutative squares, then 2-functors will preserve 2-commutative squares which can be used to define adjunctions.

No we can simply treat
$$
(-)^J:\text{CAT}\to\text{CAT}\quad\text{and}\quad E^{(-)}:\text{Cat}^\text{op}\to\text{Cat}
$$
as 2-functors.

The syntactic proof simply defines the natural bijections between the hom-sets of natural transformations.

---
# References
