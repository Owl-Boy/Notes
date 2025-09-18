---
tags:
  - Note
---
202508201608

Tags : [[Homotopy Type Theory]]
# Sum Types respect n-truncation
---
>[!theorem]
>Given an $n$-type $A:\cal U$ and a type family $B:A\to\cal U$ such that $B(a)$ is an $n$-type for all $a:A$, then the type $\sum_{a:A}B(a)$ is also an $n$-type.

For $n=-2$, we pick a centre of contraction for $a:A$, now we can consider a $b:B(a)$ which will our center of contraction, it is now easy  to compose the transports with paths in $B(a)$.

For the inductive step, for any $a:A$ we have that $B(a)$ is an $n+1$-type. To show that $\sum_{x:A}B(x)$ is an $n+1$ type, we fix $(a_{1},b_{1})$ and $(a_{2},b_{2})$.
$$
((a_{1},b_{1})=(a_{2},b_{2})) \simeq \sum_{p:a_{1}=a_{2}} (p_{*}(b_{1})=b_{2})
$$
Now we can use induction and we are done.

---
# References
- [[Dependent Pair Types|Sum Type]]
- [[n-Types]]
- [[Retract of an n-Type is an n-Type]]