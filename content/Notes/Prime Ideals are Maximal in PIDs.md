---
tags:
  - Note
  - Incomplete
---
202505211605

Tags : [[Ring Theory]]
# Prime Ideals are Maximal in PIDs
---
>[!theorem]
>Let $R$ be a [[Noetherian Ring and PIDs|PID]] and $I$ be a non-zero ideal in $R$. Then $I$ is a prime ideal, iff $I$ is also a maximal idea.

Maximal Ideals are always prime. For the other direction, let $I=(a)$ be a prime ideal in $R$. And assume that $I \subseteq J$. Since $R$ is a PID, $J=(b)$.

Therefore $a\in (b)$, that is $a=bc$ for some $c$. But then $c\in (a)$ or $b\in (a)$. If it is the latter case then we are done. 

If it is the former case then $c=ad$, that means $a=bda$, hence $bd=1$, which means $b$ is a unit thus $J=R$.

---
# References
