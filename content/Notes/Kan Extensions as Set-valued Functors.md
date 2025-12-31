---
id: Kan Extensions as Set-valued Functors
aliases:
  - Kan Extensions as Set-valued Functors
tags:
  - Note
  - Incomplete
---
202512291345

Tags : [[Category Theory]]
# Kan Extensions as Set-valued Functors
---
A [[Kan Extensions|left kan extension]] of $F:C\to E$ along $K:C\to D$ is a representation for the functor 
$$
E^C(F, K;-) : E^D\to \text{Set}
$$

that sends a functor $D\to E$ to the set of natural transformations from $F$ to its restriction along $K$. The [[Yoneda Lemma]] gives us, for any pair $(G, \gamma)$, a [[Natural Transformation]].

$$
E^D(G, -)\xRightarrow{\gamma} E^C(F, K;-)
$$

and the universal property of the pair $(\text{Lan}_K F, \eta)$ is equivalent to the assertion that the corresponding map
$$
E^D(\text{Lan}_K F, -)\xRightarrow{eta} E^C(F, K;-)
$$
is a natural isomorphism. That is $\text{Lan}_K F$ represents this functor.

This reasoning leads to the following [[Adjunctions]] on fixing a $K$.

![Kan_extension_adjunction.png](Attachments/Kan_extension_adjunction.png)

---
# References
- [[Kan Extensions]]
- [[Yoneda Lemma]]
- [[Natural Transformation]]
- [[Adjunctions]]
- [[Examples of Kan Extensions]]

