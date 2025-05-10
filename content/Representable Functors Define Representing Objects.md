---
tags:
  - Note
  - Incomplete
---
202505091505

Tags : [[Category Theory]]
# Representable Functors Define Representing Objects
---

We will not talk about a property being represented by a functor being universal, to do we get the following result using the [[Yoneda Lemma]]

>[!theorem]
>Consider a pair of object $x$ and $y$ in a locally small category:
>- If the functors represented by $x$ and $y$ are isomorphic, then $x$ and $y$ are isomorphic.

The fully faithful embeddings $C \hookrightarrow \text{Set}^{C^\text{op}}$ and the other way round create isomorphisms.
$$
C(x, -)\simeq F_{x} \simeq F_{y} \simeq C(y, -)
$$
This by [[Yoneda Embedding]] we get $x \simeq y$. If the functors were contravariant, then a similar argument would have worked with $C(-, x)$ instead. This also holds true if $x$ and $y$ represent the same functor.

this also shows that a [[Representable Functors]], defines its representing object object.



---
# References

