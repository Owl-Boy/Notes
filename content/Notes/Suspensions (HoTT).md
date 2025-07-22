---
tags:
  - Note
aliases:
  - Suspensions
---
202507150007

Tags : [[Homotopy Type Theory]]
# Suspensions
---
The **suspension** of a type $A$ is the universal way of making points of $A$ into paths (and hence paths into 2-paths and so on). 

>[!definition]
>It is denoted as $\Sigma A$ defined using the following generators:
>- a point $N:\Sigma A$
>- a point $S: \Sigma A$
>- a function $\text{merid}:A\to (N=S)$

The name suggests the image of a globe, which does hold as suspension of $\mathbb S^1$ is equivalent to $\mathbb S^2$.

The following is the recursion principle:
>[!note] Recursion Principle
>Given a type $B$ along with
>- points $n, s:B$
>- a function $m:A\to(n=s)$
>
>There exists a function $f:\Sigma A\to B$ such that $f(N)=n$ and $f(S)=s$ and for all $a:A$ we have $f(\text{merid}(a))=m(a)$.

We can also similarly define the induction principle
>[!note] Induction principle
>Given $P:\Sigma A\to\cal U$ together with:
>- a point $n:P(N)$
>- a point $s:P(S)$
>- for each $a:A$, a path $m(a):n=_{\text{merid }a}^Ps$
>
>Then there exists a function $f:\prod_{x:\Sigma A}P(x)$ such that $f(N)\equiv n$ and $f(S)\equiv s$ and for each $a:A$ we have $\text{apd}_{f}(\text{merid }a)=m(a)$

---
# References
- [[Cones and Suspensions (Topology)]]
- [[Higher Inductive Types]]
- [[Identity Type]]