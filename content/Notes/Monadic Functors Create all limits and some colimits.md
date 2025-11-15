---
tags:
  - Note
  - Incomplete
---
202510171710

Tags : [[Category Theory]]
# Monadic Functors Create all limits and some colimits
---
>[!theorem]
>A [[Monadic Functors|monadic functor]] $U:A\to C$
>- [[Preservation, Reflection and Creation of Limits|creates]] all limts
>- creates all colimts that are presereved by $T$ and $T^2$

For the first one, consider a diagram $D:J\to C^T$, spanning objects $(D_{j}, \gamma_{j})$ so that the underlying diagram $U^TD:J\to C$ admits a limit cone $\mu_{j}:L\to D_{j}$.

Then for any $C$ valued diagram $D'$ we have the natural transformation:
$$
TL\xRightarrow{T\mu}TD'\Rightarrow D'
$$
This factors uniquely through the limit cone so the following diagram commutes:![[Pasted image 20251017172914.png|200]]
for each $j$.

We will now verify that $(L, \lambda)$ is a T-algebra. We first show that the following commutes:
![[Pasted image 20251017173153.png|300]]

The back square trivially commutes, the top square commutes as $T$ is a functor, and we just showed that the bottom square commutes. Since $T$ is a monad, we know that the right triangle also commutes. Similarly we can show trivially that all but leftmost face of the following diagram commutes:

![[Pasted image 20251017174016.png|400]]

Thus we need to show that leftmost faces of both diagram commute. It suffices to prove that the diagram commutes when composed with $\mu_{j}$ for every $j$, which trivially holds.

Show that this is a limit cone is trivial, thus we are done. The same argument works for the second part with the assumption that $T$ and $T^2$ preserve colimits.

>[!theorem] Corollary
>Inclusion of a reflective subcategory creates all limits. 
>
>A category that is monadic over sets is complete, with created by the monadic forgetful functor

---
# References
- [[Monadic Functors]]
- [[Preservation, Reflection and Creation of Limits]]