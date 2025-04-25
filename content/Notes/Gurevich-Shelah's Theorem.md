---
tags:
  - Note
  - Incomplete
---
202504212004

Tags : [[Finite Model Theory]]
# Gurevich-Shelah's Theorem
---
*Gurevich-Shelah* talks about the relation between two kinds of [[Fixed Point Logics]] : $\text{LFP}$ and $\text{IFP}$. From the definitions, it is clear that $\text{LFP} \subseteq \text{IFP}$, the theorem also states that the other direction is true:

>[!theorem] Theorem: Gurevich-Shelah
>$\text{LFP}$ = $\text{IFP}$.

The idea is to construct an $\text{LFP}$ formula for each $\text{IFP}$ formula. This is done by induction, which is clearly closed under the operations given in first order logic, so we need to describe an $\text{LFP}$ formula for $\mathbf{ifp}$.

We assume the formula for which we are defining $\text{LPF}$ is also inductive, if note we define $\varphi'(R, x) = R \cup \varphi(R, x)$, then $[\mathbf{ifp}_{R,\vec{x}}\varphi(R,\vec{x})](\vec{t})$ is equivalent to

$$
\varphi((-\prec \vec{t}), \vec{t})
$$

which is stage comparison which can be defined by $\text{LFP}$, so we are done.

---
# References
