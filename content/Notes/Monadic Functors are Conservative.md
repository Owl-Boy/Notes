---
tags:
  - Note
---
202510171610

Tags : [[Category Theory]]
# Monadic Functors are Conservative
---
>[!definition]
>A functor is called **conservative** if it reflects all isomorphisms.

A *Monadic* functor is naturally equivalent to the forgetful functor from the categories of algebras for the induced monad on $C$. Thus it suffices to show that this property holds for $U^T:C^T\to C$.

A morphism $f:(A, \alpha)\to (A', \alpha')$ in $C^T$ is a map $f:A\to A'$ so the following  diagram commutes:
![[Pasted image 20251017165707.png|200]]
. But one can draw the same diagram for the inverse and paste them together.

>[!lemma] Corollary
>- A bijective continuous function between [[Compactness|compact]] [[Hausdorff Property|hausdorff]] [[Topological Spaces|spaces]] is a [[Homeomorphisms|homeomorphism]].
>- Any bijective homomorphism in a [[Category of Models for an Algebraic Theory]] is an isomorphism.



---
# References
- [[Monadic Functors]]
- [[Category of Models for an Algebraic Theory]]