---
id: Kan Extension preserving Functors
aliases:
  - Kan Extension preserving Functors
  - Left Adjoints preserve Left Kan Extensions
tags:
  - Note
---
202512311439

Tags : [[Category Theory]]
# Kan Extension preserving Functors
---
> [!DEF]
> A Functor $L:E\to F$ preserves $(\text{Lan}_K F, \eta)$ if the whiskered composite $(\text{Lan}_K, F \vartriangleright L, \eta\vartriangleright L)$ is the left [[Kan Extensions|kan extension]] of $LF$ along $K$. 

> [!EXAMPLE]
> The forgetful functor $U:\text{Top}\to \text{Set}$ has both left and right adjoints, hence preserves both limits and colimits. If follows that $U$ preserves the left and right kan extensions.

> [!THM] Theorem
> Left adjoints preserve left Kan extensions.

If $L$ has a right adjoint $R$ with unit $\iota$ and counit $\nu$, Then Given $H:D\to F$, there are natural isomorphisms 
$$
F^D(L\text{Lan}_K F, H)\cong E^D(\text{Lan}_K F, RH)\cong E^C(F, RHK)\cong F^C(LF, HK)
$$

Taking $H=\text{Lan}_K F \vartriangleright L$ These natural isomoprhisms take $1_{\text{Lan}_K F\vartriangleright L}$ to $\eta\vartriangleright L$

---
# References
- [[Kan Extensions]]
- [[Adjunctions]]

