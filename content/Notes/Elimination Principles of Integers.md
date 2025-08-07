---
tags:
  - Note
---
202507291607

Tags : [[Homotopy Type Theory]]
# Elimination Principles of Integers
---
We will be use the first definition of integers in [[Integers in HoTT]]. 

This is the induction principle that we will be deriving from rules of [[Set Quotient]].

>[!note] Induction principle.
>Suppose $p:\mathbb{Z}\to\cal U$ is a type family and that we have
>- $d_{0}:P(0)$
>- $d_{+}:\prod_{k:\mathbb{N}}P(k)\to P(\text{suc }k)$ and
>- $d_{-}:\prod_{k:\mathbb{N}}P(-k)\to P(\text{suc }-k)$
> 
>then we have $f:\prod_{z:\mathbb{Z}}P(z)$ such that:
>- $f(0)=d_{0}$
>- $f(\text{suc }k)=d_{+}(k, f(k))$ for all $k:\mathbb{N}$
>- $f(-\text{suc }k)=d_{-}(k, f(-k))$ for all $k:\mathbb{N}$.

Let $\mathbb{Z}:\equiv \sum_{(x:\mathbb{N}\times \mathbb{N})}r(x)=x$, where $r$ is the idempotent we have from [[Idempotent from a relation on a type]]. Let $q:\mathbb{N}\times \mathbb{N}\to \mathbb{Z}$ be the quotient map, defined by $q(x)=(r(x),i(x))$. Now define $Q=P\circ q:\mathbb{N}\times \mathbb{N}\to\cal U$. By transporting the given data across appropriate equalities, we obtain:
$$
\begin{align}
d'_{0}&:Q(0,0) \\
d'_{+}&:\prod_{k:\mathbb{N}}Q(k, 0) \to Q(\text{suc }k, 0)\\
d'_{-}&:\prod_{k:\mathbb{N}}Q(k, 0) \to Q(0, \text{suc }k)
\end{align}
$$

Since $q(n,m)=q(\text{suc }n,\text{suc }m)$ we have the induced equivalence:
$$
e_{n,m}:Q(n, m) \simeq Q(\text{suc }n,\text{suc }m)
$$
Thus we can construct $g:\prod_{(x:\mathbb{N}\times \mathbb{N})}Q(x)$ by double induction on $x$:
$$
\begin{align}
g(0,0)&:\equiv d'_{0} \\
g(\text{suc }k,0)&:\equiv d'_{+}(k, g(n,0))\\
g(0,\text{suc }k)&:\equiv d'_{-}(k, g(0,k)) \\
g(\text{suc }n,\text{suc }m)&:\equiv e_{n,m}(g(n, m))
\end{align}
$$
 

---
# References
- [[Integers in HoTT]]
- [[Set Quotient]]
- [[Idempotent from a relation on a type]]