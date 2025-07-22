---
tags:
  - Note
  - Incomplete
---
202506201706

Tags : [[Module Theory]]
# R-Mod is a CCC
---
>[!theorem]
>$R$-Mod is a [[Cartesian Closed Category]], under [[Direct sum of Modules]] and the internal hom functor.

## $R$-Mod is monoidal under direct sum
There is a unit object $\mathbf{0}$ such that $0 \oplus M\cong M\cong M \oplus \mathbf{0}$ where the isomorphism is just the projections, which are trivially natural.
  
Given $R$-mods $M, N, O$, we have 
$$
(M \oplus N) \oplus O \cong M \oplus (N \oplus O)
$$
that sends $((m, n),o)$ to $(m, (n, o))$. This map is also trivially natural.

Checking if the coherence diagrams commute is also trivial.

## $R$-Mod is Closed
Given $2$ modules $M, N$ the set $\text{Hom}(M, N)$ is an abelian group because $M, N$ can be thought of as abelian groups, and it can then be enriched with an $R$-structure by multiplicatoin in the image.

Rest seems too much work, but I think it holds T-T.

## $R$-Mod is Cartesian closed
We need to show
$$
\text{Hom}(M \times N, O) \cong \text{Hom}(M, \text{Hom}(N, O))
$$
This can be done by considering a morphism $\varphi:M \times N \to O$ we can send it to the morphism $\varphi': m \mapsto \varphi(m, -)$.

This map is a module homomorphism too, so it works out and is natural.



---
# References
