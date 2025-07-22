---
tags:
  - Note
  - Incomplete
---
202506211906

Tags : [[Module Theory]]
# If $R$ is [[Noetherian Ring and PIDs|Noetherian]] and $M$ is finitely generated then $M$ is [[Noetherian Modules|Noetherian]]
---
This is a corollary of the theorem discussed [[M is noetherian if for every sub-module N, N and MN are noetherian|here]].
>[!lemma] Corollary
>If $R$ is [[Noetherian Ring and PIDs|Noetherian]] and $M$ is finitely generated then M is [[Noetherian Modules|Noetherian]].

We have an onto morphism $R^{\oplus n}\twoheadrightarrow M$. Hence $M$ is isomorphic to a quotient of $R^{\oplus n}$. By the mentioned theorem we need to show that $R^{\oplus n}$ is finitely Noethrian.

This can be done by induction. Since $R$ is [[Noetherian Ring and PIDs|Noetherian]] as a ring, it is [[Noetherian Modules|Noethrian]] as a module. Now to show that $R^{\oplus n}$ is Noetherian, we show that $R^{\oplus (n-1)}$ is noetherian, which is again enough by the given theorem since 
$$
\frac{R^{\oplus n}}{R^{\oplus (n-1)}} \cong R
$$
which we have by induction hypothesis. so we are done.

---
# References
- [[Noetherian Ring and PIDs]]
- [[Noetherian Modules]]
- [[M is noetherian if for every sub-module N, N and MN are noetherian]]