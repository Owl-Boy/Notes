---
tags:
  - Note
  - Incomplete
---
202505151705

Tags : [[Ring Theory]]
# Zero Divisors
---
>[!definition]
>A **Zero Divisor** in a ring $R$ is an element $a$ such that there exists a non-zero element $b$ such that $ab=0$. Specifically, $a$ here, is a *left-zero-divisor*.

>[!lemma]
>In a  ring $R$, $a\in R$ is a not a *left-zero-divisor* iff the function $(a \cdot -)$ is an injective function.

Proof is fairly straightforward:
- If $a$ is a *left-zero-divisor*, then there is a non-zero element $b$ such that $ab=0$, but we have $a \cdot 0 = 0$ hence left multiplication by $a$ is not injective.
- If left multiplication by $a$ is not injective, then there are elements $b\neq c$ such that $ab=ac$, But we then have $a(b-c)=0$ where $b-c$ is not $0$, hence $a$ is a left-zero-divisor.


---
# References
