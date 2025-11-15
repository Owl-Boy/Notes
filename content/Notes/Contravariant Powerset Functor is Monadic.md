---
tags:
  - Note
---
202510171610

Tags : [[Category Theory]]
# Contravariant Powerset Functor is Monadic
---
$\text{Set}$ is a [[Cartesian Closed Category]], thus we have 
$$
(A \to PB) \simeq (A\times B \to \mathbf{2}) \simeq (B\to PA)
$$
The functor $P$ is a left-adjoint to itself. Since [[Set is Complete]], it has finite limits, but in particular, equalizers of coreflexive pairs, which proves the first point of [[Reflexive Tripleability Theorem]],

But given the following equalizer diagram:
![[Pasted image 20251017162414.png|250]]

The existence of a retract indicates that $f$ and $g$ are monic, thus we get the following pullback diagram of monics:
![[Pasted image 20251017162508.png|200]]

Using [[Lemma for Monadicity of Contravariant Powerset Functor]] we get 
![[Pasted image 20251017162608.png|300]]
 is a [[Split Coequalizer]] diagram, which proves point 2 of [[Reflexive Tripleability Theorem]].

Note that $P$ is faithful, given a parallel pair of functions $f, g:A\to B$, the composites:
![[Pasted image 20251017163302.png|300]]
with the singleton map define $(A\times B\to \mathbf{2})$. It follows from the universal property of the [[Subobjects|sub-object classifier]] that if $f^{-1}=g^{-1}$ then $f=g$. And since in sets, any faithful functor refects monomorphism and epimorphisms, we get that the isomorphism are reflected.

---
# References
- [[Cartesian Closed Category]]
- [[Set is Complete]]
- [[Reflexive Tripleability Theorem]]
- [[Subobjects]]
- [[Split Coequalizer]]