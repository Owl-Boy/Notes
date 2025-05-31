---
tags:
  - Note
---
202505261705

Tags : [[Homotopy Type Theory]]
# Total Spaces
---
>[!definition]
>Given type families $P, Q:A \to \cal U$ and a map $f:\prod_{a:A}P(x)\to Q(x)$ we define:
>$$
>\text{total}(f) :\equiv \lambda w.(\text{pr}_{1}(w), f(\text{pr}_{1}w, \text{pr}_{2}w)) : \sum_{x:A}P(x) \to \sum_{x:A}Q(x)
>$$

>[!theorem]
>Suppose $f$ is a fiberwise transformation between families $P$ and $Q$ over a type $A$, let $x:A$ and $v:Q(x)$ then we have:
>$$
>\text{fib}_{total(f)}((x, v)) \simeq \text{fib}_{f(x)}(v)
>$$

^cf9900

Proof is annoying calculations:
$$
\begin{align}
\text{fib}_{\text{total}(f)}((x, v)) &\equiv \sum_{w:\sum_{x:A}P(x)} (\text{pr}_{1}w,f(\text{pr}_{1}w, \text{pr}_{2}w))=(x, y) \\
&\simeq \sum_{a:A}\sum_{u:P(a)} (a, f(a, u))=(x,v) \\
&\simeq \sum_{a:A}\sum_{u:P(a)} \sum_{p:a=x}p_{*}(f(a, u))=v\\
&\simeq \sum_{a:A}\sum_{p:a=x}\sum_{u:P(a)} p_{*}(f(a, u))=v \\
&\simeq \sum_{u:P(x)} f(x, u)=v \\
&\equiv \text{fib}_{f(x)}(v)
\end{align}
$$

---
# References
- [[Fibers (HoTT)]]