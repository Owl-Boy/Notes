---
tags:
  - Note
---
202501310001

Tags : [[Finite Model Theory]]
# Gaifman-Locality implies BNDP
---
>[!theorem]
>Let $Q$ be a [[Gaifman-Locality|Gaifman Local]] $m$-ary query, $m>0$. Then $Q$ has [[Bounded Number of Degrees Property|BNDP]]. 

Let $Q$ be [[Gaifman-Locality|gaifman-local]] with $\text{lr}(Q)=d$.  We assume, wlog $m \geq 2$ and then we use the following claim

>[!lemma] Claim
>Let $\vec{a}\approx_{n_{d}(k)}^\mathfrak A \vec{b}$ then there is a bijection $f: A^k \to A^k$ such that $\vec{a}\vec{c}\approx_{n_{d}(k)}^\mathfrak A \vec{b}\vec{c}$  for every $\vec{c}\in A^k$.

where $n_{d}(0)=d$ and $n_{d}(k+1)=3 \cdot n_{d}(k)+1$.

To prove the claim we simply induct, base case when $k=0$ is trivial, assume it works for $k$, we prove it for $k+1$.

So we have $\vec{a}\approx_{3 \cdot n_{d}(k)+1}^\mathfrak A \vec{b}$, so by [[Local Equivalence Lemma]] we have $\vec{a}c \approx_{n_{d}(k)}^\mathfrak A \vec{b}g(c)$, and by the induction hypothesis we have $\vec{a} c \vec{c}\approx_{d}^\mathfrak A \vec{b} g(c)g_{c}(\vec{c})$, and we define $f(c)=g(c)g_{c}(\vec{c})$. This proves the claim.

Now to show BNDP:
For every vocabulary $\sigma$, there exists a function $G_{\sigma}: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ such that for every $\mathfrak A \in \text{STRUCT}_{l}[\sigma]$ we define $G_{\sigma}(l, d)$ to be the size of the largest $d$ Ball in $\frak A$. So there exists $F_{\sigma}: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ which is the number of isomorphism types of $d$-neighborhoods of a point.

Now consider $Q(\mathfrak A)$ for some $\mathfrak A\in \text{STRUCT}_{l}(\sigma)$ and for any 2 $a, b$ with $a \approx_{n_{d}(m-1)}^\mathfrak A b$, by the above claim we get
$$
|\{ \vec{c}\in A^{m-1} |\ a \vec{c}\in Q(\mathfrak A) \}| = |\{ \vec{c}\in A^{m-1} |\ b \vec{c}\in Q(\mathfrak A) \}|
$$
This claims that degrees of $\vec{a}$ and $\vec{b}$ are the same. This the number of different degrees in $Q(\mathfrak A)$ corresponding to the first position in the $m$-tuple is at most $F_{\sigma}(l, n_{d}(m-1))$
hence
$$
|\text{deg\_set}(Q(\mathfrak A))| = | m \cdot F_{\sigma}(l, n_{d}(m-1))|
$$

This has the following nice result

>[!lemma] Corollary
> Every $\text{FO}$-definable query has BNDP.

---
# References
