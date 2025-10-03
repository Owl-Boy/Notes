---
tags:
  - Note
  - Incomplete
---
202509201509

Tags : [[Homotopy Type Theory]]
# Sum of n-types is an n-type
---
>[!theorem]
>Let $P:A\to\cal U$ be a family of types. Then there is an equivalence
>$$
>\Big\|\sum_{x:A}\|P(x)\|_{n} \Big\|_{n} \simeq \Big\|\sum_{x:A}P(x)\Big\|_{n}
>$$

We use induction principle of $n$-truncation may times to compute the following functions:
$$
\phi :\Big\|\sum_{x:A}\|P(x)\|_{n} \Big\|_{n} \to\Big\|\sum_{x:A}P(x)\Big\|_{n}
$$
- We first make function from $(\sum_{x:A}P(x))\to \|\sum _{x:A} P(x)\|$. 
- This gives us product of functions $\prod_{x:A}P(x)\to \|\sum_{x:A}P(x)\|$, 
- and  by induction principle of truncation, we get a function $\prod_{x:A}\|P(x)\|\to\|\sum_{x:A}P(x)\|$, 
- which gives a function $\left( \sum_{x:A}\|P(x)\| \right)\to \|\sum_{x:A}P(x)\|$, 
- which by induction principle of n types gives a function $\|\sum_{x:A}\|P(x)\|\|\to\|\sum_{x:A}P(x)\|$.
- This definition gives $\phi(|(x,|u|_{n})|_{n}):\equiv|(x,u)|_{n}$

And now we construct another function of type:
$$
\psi :\Big\|\sum_{x:A}P(x)\Big\|_{n} \to\Big\|\sum_{x:A}\|P(x)\|_{n} \Big\|_{n}
$$
- Dude to similar reasoning, we can define $\psi(|x, u|_{n}):\equiv|(x,|u|_{n})|_{n}$.

To show that this forms an equivalence, we need to define homotopies $H:\phi\circ \psi \sim \text{id}$ and $K:\psi\circ\phi \sim\text{id}$. Both are refl, (also use induction principle for n-truncations to define it.)

>[!theorem] Corollary
>If $A$ is an $n$-type and $P:A\to \cal U$ is any type family, then 
>$$
>\sum_{x:A}\|P(a)\|_{n} \simeq \Big\|\sum_{a:A}P(a)\Big\|_{n}
>$$

---
# References
- [[Homotopy(HoTT)]]
- [[Truncation]]