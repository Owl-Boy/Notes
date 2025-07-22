---
tags:
  - Note
---
202507061607

Tags : [[Ring Theory]]
# Associates in Rings
---
Consider a ring $R$ with elements $a$ and $b$
>[!definition]
>We say that $a,b$ are associates if $(a)=(b)$, that is $a|b$  and $b|a$.

>[!lemma] 
>If $R$ is an [[Integral Domain]] then $a$ and $b$ are associates iff $a=ub$ for a unit $u$ in $R$.

This is simple, let $a=bc$ and $b=ad$, then we have:
$$
a = bc = adc
$$
and we get 
$$
\begin{align}
a - a &= 0 \\
a-adc &= 0 \\
a(1-cd) &= 0 \\
cd&=1
\end{align}
$$
The final step works because $R$ is an integral domain, and we get that $c$ and $d$ are units.

For the other direction let $a=ub$, since $u$ is a unit, we have $vu=1$ for some $v$ the we have $va=b$. so $a|b$ and $b|a$.

>[!attention]
>This is not necessarily true when $R$ is not an integral domain, consider the ring $\mathbb{Z} /6\mathbb{Z}$. Here we have that $4_{6}=2_{6}\cdot 2_{6}$. Here we have that $4$ and $2$ are associates.



---
# References
- [[Integral Domain]]