---
tags:
  - Note
  - Incomplete
---
202412020412

Tags : [[Algebraic Automata Theory]]
# Green's Relations
---
>[!definition] Pre-Green's Relations
>Let $\mathcal M = (M, *, 1)$ be a monoid, then the relations $\leq_{L}, \leq_{R}, \leq_{J}$ are defined as folows
>$$
>\begin{align}
>s \leq_{L} t &\triangleq \exists u.\ s=ut \\
>s \leq_{R} t &\triangleq \exists u.\ s=tu \\
>s \leq_{J} t &\triangleq \exists u,v.\ s=utv \\
>\end{align}
>$$

*Note:* $\leq_{J} = \leq_{L} \circ \leq_{R} = \leq_{R}\circ \leq_{L}$.

>[!definition] Green's Relations
>Let $\mathcal M = (M, *, 1)$ be a monoid, then the relations $\cal L, R, J$ are defined on it as follows
>$$
>\begin{align}
>s \mathcal {L} t &\triangleq s \leq_{L} t \text{ and } t \leq _{L} s\\
>s \mathcal {R} t &\triangleq s \leq_{R} t \text{ and } t \leq _{R} s\\
>s \mathcal {J} t &\triangleq s \leq_{J} t \text{ and } t \leq _{J} s\\
>s \mathcal {H} t &\triangleq s \leq_{H} t \text{ and } t \leq _{H} s\\
>\end{align}
>$$

>[!lemma]
>Over any finite monoid, $\cal J = L \circ R = R \circ L$

**Proof:** containment of last 2 in $\mathcal J$ is easy, the other side requires work.
Let $s \mathcal J t$, so $s=utv$ and $t=xsy$. substitute to get $s = uxsyt$ and let $N$ be the idempotent power of $ux$, so we get $s=(ux)^Ns$ so $xs \mathcal L s$. similarly $s \mathcal R sy$, therefore $s \mathcal {L\circ R}\ xsy=t$. and vice versa.

>[!lemma]
>Over any finite monoid
>- If $s \mathcal J t$ and $s \leq_{L} t$ then $s\mathcal L t$
>- If $s \mathcal J t$ and $s \leq_{R} t$ then $s\mathcal R t$

**Proof:** Suppose $s \leq_{R} t$, then $s = tu$ and $t = xsy$, then we get $t = xtuy$ and let $N$ be the idempotent power of $uy$, so we get $t = t(uy)^N$ so $t = tu.y.(uy)^N$ thefore $t = sy(uy)^N$, so $t \leq_{R} s$, the other side can be proved similarly.

---
# References
[[Green's Lemma]]