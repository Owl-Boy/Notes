---
tags:
  - Note
---
202509222009

Tags : [[Homotopy Type Theory]]
# Maps between Cocones
---
Consider the following span $\mathcal D :\equiv (A, B, C, f, g)$ along with a cocone $c:\equiv(i, j, h):\text{cocone}_{\cal D}(D)$, which can be drawn as:
![[Pasted image 20250922201928.png|150]]

We will now first consider maps of the form $t:D\to E$, which can be converted to maps from $\text{cocone}_{\cal D}(D)\to\text{cocone}_{\cal D}(E)$, also the map $\text{cocone}_{\cal D}(-)$ is functorial (covariant), which looks as follows:

>[!todo] draw diagram

Now we consider maps between the spans, Given a span $\mathcal D\equiv(A, B, C, f, g)$ and $\mathcal D' \equiv(A',B',C', f',g')$, a map between $\cal D \to \cal D'$ would be $(\alpha,\beta,\gamma, \phi, \psi)$
 where
 - $\alpha:A\to A'$
 - $\beta:B\to B'$
 - $\gamma:C\to C'$
 - $\phi:\alpha\circ f \sim f'\circ\gamma$
 - $\psi:\beta\circ g\sim g'\circ\gamma$
which looks as follows:

>[!todo] draw diagram.

Any such map can be used to construct a map between cocones of the following type: $\text{cocone}_{\cal D'}(D)\to\text{cocone}_{\cal D}(D)$. And the map $\text{cocone}_{(-)}(D)$ is functorial (contravariantly).

Both of these functions also compose well, that is the following diagram commutes:
![[Pasted image 20250922203037.png|300]]

The proof of this theorem is simply stating that in the following diagram, extending upwards and then extending downwards is the same as extending downwards and then extending upwards.

>[!todo] draw diagram

---
# References
- [[Cocones (HoTT)]]
- [[Functors]]