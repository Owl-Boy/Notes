---
tags:
  - Note
  - Incomplete
---
202412020512

Tags : [[Algebraic Automata Theory]]
# Green's Lemma
---
>[!lemma] 
>Let $\mathcal M$ be a finite monoid and let $s \mathcal J t$, then 
>- If $s \mathcal R t$ and $su = t$ and $tv = s$ then maps $(*u)$ and $(*v)$ are bijections between $\mathcal L(s)$ and $\mathcal L(t)$. And they preserve the $\cal H$ classes.
>- If $s \mathcal L t$ and $us = t$ and $vt = s$ then maps $(u*)$ and $(v*)$ are bijections between $\mathcal R(s)$ and $\mathcal R(t)$. And they preserve the $\cal H$ classes.

$\cal L$ is congruent with right multiplication so $*u$ maps $\mathcal L(s)$ to $\mathcal L(t)$. For any $x\in \mathcal L(s), x=ys$ so $xuv = ysuv=ys=x$, so the maps are inverses of each other.

Also $xu \leq_{L} x$, so $\cal H$-classes are mapped to $\cal H$ classes. The other direction is proved similarly.

---
# References
