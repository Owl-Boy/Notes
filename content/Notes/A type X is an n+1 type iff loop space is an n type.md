---
tags:
  - Note
---
202508280108

Tags : [[Homotopy Type Theory]]
# A type $X$ is an $(n+1)$-type iff loop space is an $n$-type
---
We first prove the lemma
>[!lemma]
>Given $n\geq -1$ and $X:\cal U$, if a given inhabitant of $X$ proves that $X$ is an $n$-type then $X$ is an $n$-type.

Let $f:X\to\text{is-n-type}(X)$. We show that for any $x, x'$, the type $x=x'$ is an $n-1$ type. But $f(x)$ shows that $x$ is an $n$-type, hence all its path spaces are $n-1$ types.

>[!theorem]
>For any $n\geq{-1}$ a type $X$ is an $(n+1)$-type iff for all $x:X$ the type $\Omega(X,x)$ is an $n$-type.

The only if direction is obvious. Conversely, to show that $X$ is an $(n+1)$-type, we need to show that $x=x'$ is an $n$-type and by the previous lemma we only need to show 
$$
(x=x')\to\text{is-n-type}(x=x')
$$
By path induction, it suffices to show when $x\equiv x'$, in which case we just have our asssumption.

>[!theorem] Corollary
>For every $n\geq -1$, a type $A$ is an $n$-type iff $\Omega^{n+1}(A,a)$ is contractible for all $a:A$.

The type $\Omega^0(A, a)=(A, a)$, so we are done. The case when $n=0$ is just [[A type is a set iff it satisfies axiom K]]. We now use induction.

By the above theorem, $A$ is an $(n+1)$-type iff $\Omega(A, a)$ is an $n$-type, which is equivalent to saying that $\Omega^{n+1}(\Omega(A,a),p)$ is contractible for all $p:\Omega(A, a)$.

Since $\Omega^{n+2}(A, a):\equiv \Omega^{n+1}(\Omega(A, a), \text{refl}_{a})$ and $\Omega^{n+1}=\Omega^n\circ \Omega$, we only need to show that $\Omega(\Omega(A, a),p)$ is equal to $\Omega(\Omega(A, a), \text{refl}_{a})$. For that we give an equivalence
$$
g:\Omega(\Omega(A,a), p) \simeq \Omega(\Omega(A,a),\text{refl}_{a})
$$
For $q:p=p$ we define $g(q):\text{refl}_{a}=\text{refl}_{a}$ to be the following
$$
\text{refl}_{a}=p \cdot p^{-1} \overset{\text{ap}_{\lambda r.r\cdot p^{-1}}(q)}{=} p \cdot p^{-1}=\text{refl}_{a}
$$
that is, we get this by composing both sides of $q$ by $p^{-1}$ and noticing that this can be thought of as a whisker for $\text{refl}_{a}=\text{refl}_{a}$.

This is going to be an equivalence because it an composition of equivalences
$$
(p=p)\xrightarrow{\text{ap}_{\lambda r.r\cdot p^{-1}}}(p\cdot p^{-1}=p\cdot p^{-1})\xrightarrow{i\cdot-\cdot i^{-1}}(\text{refl}_{a}=\text{refl}_{a})
$$

---
# References
- [[A type is a set iff it satisfies axiom K]]