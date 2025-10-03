---
tags:
  - Note
---
202509231609

Tags : [[Homotopy Type Theory]]
# Characterizing n connectedness using n-types
---
>[!theorem]
>For $f:A\to B$ and $P:B\to\cal U$, consider the following function:
>$$
>\lambda s.s\circ f : \left( \prod_{b:B}P(b) \right) \to \left( \prod_{a:A}P(f(a)) \right)
>$$
>For a fixed $f$ and $n\geq -2$, the following are equivalent:
>- $f$ is $n$-connected.
>- For every $P:B\to n$-type, the map $\lambda s.s\circ f$ is an equivalence
>- For every $P:B\to n$-type, the map $\lambda s.s\circ f$ has a section

Suppose $f$ is $n$-connected and $P:B\to n$-type, then we have the following equivalences.

$$
\begin{align}
\prod_{b:B}P(b) &\simeq \prod_{b:B}\|\text{fib}(b)\|_{n} \to P(b)\\
&\simeq \prod_{b:B}\text{fib}(b) \to P(b)\\
&\simeq \prod_{b:B}\prod_{a:A}\prod_{p:f(a)=b}P(b) \\
&\simeq \prod_{a:A}P(f(a))
\end{align}
$$

So we have 1 -> 2 and 2 -> 3, now we need to show 3->1.

Consider the type family
$$
P(b):\equiv \|\text{fib}_{f}(b)\|_{n}
$$
Then we have a map $c:\prod_{b:B}\|\text{fib}_{f}(b)\|_{n}$ with $c(f(a))=|(a, \text{refl}_{f(a)})|_{n}$

Now we need to show that $\|\text{fib}_{f}(b)\|_{n}$ is contractible. So we need a function of type
$$
\prod_{b:B}\prod_{w:\|\text{fib}_{f}(b)\|_{n}}w=c(b)
$$
and it suffices to find a function of type
$$
\prod_{b:B}\prod_{a:A}\prod_{p:f(a)=b}|(a, p)|_{n}=c(b)
$$
But we can rearrange variables and use path induction to get
$$
\prod_{a:A}|(a, \text{refl}_{f(a)})|_{n}=c(f(a))
$$
which holds as $c$ has a section.

>[!theorem] Corollary
>The canonical function $|-|_{n}:A\to\|A\|_{n}$ is $n$-connected

>[!theorem] Corollary
>A type $A$ is $n$-connected iff the map
>$$
>\lambda ba.b:B\to A\to B
>$$
>is an equivalence for every $n$-type $B$. Every map from $A$ to an $n$-type is constant.

---
# References
- [[n-Types]]
- [[n-connected types]]