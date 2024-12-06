---
tags:
  - Note
  - Incomplete
---
202412020512

Tags : [[Algebraic Automata Theory]]
# Location Lemma
---
>[!theorem]
>Let $\cal M$ be a finite monoid and let $s\mathcal J t$, then $st \mathcal J s$ iff $\mathcal L(s)\cap \mathcal R(t)$ contains an idempotent

if $e\in \mathcal L(s)\cap \mathcal R(t)$ is idempotent then $xe = s$,  and $ey=y$ so $se = s$ and $et=t$, so by [[Green's Lemma]] we have $*t$ as a bijection and we get $st$ in the correct placr.

If $st\mathcal J s$ then by green's lemma, $*t$ is a bijection on $\mathcal L(s)$ so there is an $x$ such that $xt = t$ and there is a $y$ such that $x = ty$ but we get $tyt=t$ hence $tyty=ty$. Therefore $x$ is an idempotent.

---
# References
[[Green's Lemma]]