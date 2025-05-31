---
tags:
  - Example
---

202503290010

tags : [[Homotopy Type Theory]]

#  Addition is Associative
---
We define addition for natural numbers as:
$$
\begin{align}
0 + n &\equiv n \\
\text{succ}\ m + n &\equiv \text{succ}\ (m + n)
\end{align}
$$
as defined in [[Natural Numbers in Type Theory#^5e069a]]

We shall prove the following theorem
>[!theorem] Theorem: Associativity
>$$
>\text{assoc} :  \prod_{i,j,k: \mathbb{N}} (i+j)+k = i+(j+k)
>$$

The induction principle states that it is sufficient to supply a proof for:
$$
\text{assoc}_{0} : \prod_{j, k:\mathbb{N}}(0+j)+k = 0+(j+k)
$$
and 
$$
\begin{align}
\text{assoc}_{s}:\prod_{i:\mathbb{N}}&\left( \prod_{j, k:\mathbb{N}}(i+j)+k = i+(j+k) \right) \to \\&\left( \prod_{j, k:\mathbb{N}}(\text{succ}(i)+j)+k = \text{succ}(i)+(j+k) \right)
\end{align}
$$

To prove $\text{assoc}_{0}$ remember that by definition of $+$ we get $0+n \equiv n$ so we have 
$$
(0+j)+k \equiv j+k \equiv 0+(j+k)
$$
hence  we can define 
$$
\text{assoc}_{0}(j, k) :\equiv \text{refl}_{j+k} 
$$
Now we need to define $\text{assoc}_{s}$ and by definition of $+$ we get $\text{succ}(n)+m \equiv \text{succ}(n+m)$, so we have
$$
\begin{align}
(\text{succ}(i)+j)+k &\equiv \text{succ}(i+j)+k  \\
&\equiv \text{succ} ((i+j)+k)
\end{align}
$$
And since we are assuming that $(i+j)+k = i+(j+k)$ so we get
$$
\begin{align}
\text{succ}((i+j)+k) &= \text{succ}(i+(j+k)) \\
&\equiv \text{succ}(i)+(j+k)
\end{align}
$$

We now somehow need to use the equality inside successor, for this we use a function defined for equality that we will discuss later called 
$$
\text{ap}_{f}: (m=n) \to f(m)=f(n).
$$
so we get 
$$
\text{assoc}_{s}(i, h, j, k) :\equiv \text{ap}_{\text{succ}}(h(h, k))
$$
And we are done.

---
# Related
[[Natural Numbers in Type Theory]]