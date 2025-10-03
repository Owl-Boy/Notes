---
tags:
  - Note
---
202509201609

Tags : [[Homotopy Type Theory]]
# n truncations of path space is path space of n+1 truncation
---

>[!theorem]
>For any $A$ and $x, y:A$ and $n\geq -2$, the map defined in [[Sum of n-types is an n-type]] is an equivalence, thus we have 
>$$
>\|x=y\|_{n} \simeq \left( |x|_{n+1}=|y|_{n+1} \right) 
>$$

The direction from left to right is given simply by 
$$
\begin{matrix}
f&: & \|x=y\|_{n}  & \to &  (|x|_{n+1}=|y|_{n +1}) \\
f&:\equiv & \lambda |p|_{n} & \mapsto & \text{ap}_{|-|_{n+1}}(p)
\end{matrix}
$$
For the other direction, we cannot induct on equality $|x|_{n+1}=|y|_{n+1}$ so we have to generalise to include all of $\|A\|_{{n+1}}$. For that we define $P:\|A\|_{n+1}\to\|A\|_{n+1}\to\text{n-Type}$, which we define as
$$
P(|x|_{n+1},|y|_{n+1}):\equiv\|x=y\|
$$

Now for every $u, v:\|A\|_{n+1}$ we have the map:
$$
\text{decode}:P(u, v)\to (u=v)
$$
which is defined for $|x|_{n+1}$ and $|y|_{n+1}$ and $p:(x=y)$ as $\text{ap}_{|-|_{n+1}}(p)$. We also define
$$
r:\prod_{u:\|A\|_{n+1}}P(u,u)
$$
and by induction on $u$ we only need to define it for the case of $|x|$, for which we can give $|\text{refl}_{x}|$.

Now we can define the map 
$$
\text{encode}:(u=v)\to P(u, v)
$$
by
$$
\text{encode}(p):\equiv \text{transport}^{v\mapsto P(u, v)}(p, r(u))
$$

ow we need to show that the composite $\text{decode}\circ\text{encode}$ is the identity function, but that is trivial from path induction and then induction on n-type, we get it directly.

Now we need to show that $\text{encode}\circ\text{decode}$ gives identity function.

Here since goal is an $n-1$ type, we can assume that $u=|x|_{n+1}$ and $v=|y|_{n+1}$ and we are considering $|p|:P(|x|_{n+1},|y|_{n+1})$ where $p:x=y$, then we have:
$$
\begin{align}
\text{encode}(\text{decode}(|p|_{n})) &= \text{encode}(\text{ap}_{|-|_{n+1}}(p)) \\
 & =\text{transport}^{v\mapsto P(|x|_{n+1},v)}(\text{ap}_{|-|_{n+1}}(p),|\text{refl}_{x}|_{n}) \\
 & =\text{transport}^{y\mapsto\|x=y\|_{n}}(p, |\text{refl}_{x}|_{n}) \\
 & =\Big|\text{transport}^{y\mapsto(x=y)}(p, \text{refl}_{x})\Big| \\
 & =|p|_{n}
\end{align}
$$

And so we are done.

>[!theorem] Corollary
>Let $n\geq-2$ and $k\geq0$ and $(A, a)$ be a [[Pointed Type]], Then
>$$
>\|\Omega^k(A,a)\|_{n}=\Omega^k(\|(A, a)\|_{n+k})
>$$



---
# References
- [[Sum of n-types is an n-type]]
- [[Sum Types respect n-truncation]]
- [[Pointed Type]]