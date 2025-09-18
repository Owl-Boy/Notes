---
tags:
  - Note
---
202508272308

Tags : [[Homotopy Type Theory]]
# Axiom K
---
**Axiom K** is an elimination rule for equality types that was added by _Thomas Streicher_ in 1993 which when added to intentional type theory converts it to set level type theory, the axiom infomally states:

>[!axiom]
> Given any type $A$ and any element $x:A$, the type $x=x$ is inhabited by exactly 1 element, which is $\text{refl}_{x}$.

Formally, the axiom writes as:
$$
K : \prod_{(A:\mathcal U)} \prod_{(x:A)} \prod_{(P:x=x\to\mathcal U)} P(\text{refl}_{x}) \to \prod_{h:x=x}P(h)
$$

This reads as, given any type $A$ and any $x:A$ and any type family over $x=x$, to define a function out of the type family, it suffices to define it for $\text{refl}_{x}$. Since $\text{refl}_{x}$ cannot generate any elements other than itself, this states that all witness of equality of $x$ are propositionally equal.


---
# References
- [Streicher 1993](https://www2.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf)
- [[Identity Type]]