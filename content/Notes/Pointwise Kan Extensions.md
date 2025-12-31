---
id: Pointwise Kan Extensions
aliases:
  - Pointwise Kan Extensions
tags:
  - Note
---
202512311455

Tags : [[Category Theory]]
# Pointwise Kan Extensions
---
> [!DEF] Definition 
> When $E$ is locally small, a right [[Kan Extensions|kan Extensions|kan extension]] is a *pointwise* kan extension if it is preserved bt all representable functors $E(e, -)$.

> [!THM] Theorem 
> A right Kan extension of $F$ along $K$ is pointwise if and only if it can be constructed by the following:
> $$
> \text{Ran}_K F = \lim \left(d / K \xrightarrow {\Pi_d^K} C \xrightarrow F E \right)
> $$
> in which case, this limit exists.

If $\text{Ran}_K F$ is pointwise, then by [[Yoneda Lemma]] and the defining universal property of Kan Extensions 
$$
\begin{align}
E(e, \text{Ran}_K F)&\cong \text{Set}^D(D(d,-), E(e, \text{Ran}_K F))\\
&\cong \text{Set}^C(D(d, K-), E(e, F-))\\
&\cong \text{Cone}(E, F\Pi_d^K) 
\end{align}
$$

---
# References

- [[Kan Extensions]]
- [[Yoneda Lemma]]
