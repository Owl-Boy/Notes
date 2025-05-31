---
tags:
  - Note
  - Incomplete
---
202505211605

Tags : [[Ring Theory]]
# Prime Ideals and Maximal Ideals
---
>[!definition]
>Let $I$ be a proper ideal of the commutative ring $R$.
>- $I$ is called a **Prime Ideal** if $R/I$ is an [[Integral Domain]]
>- $I$ is called a **Maximal Ideal** if $R /I$ is a [[Fields|Field]]

The names do make sense because they satisfy the following property:
>[!lemma]
>Given a proper ideal $I$ of a commutative ring $R$
>- $I$ is prime iff for all $a, b\in R$ we have $ab=I$ iff $a \in I$ or $b \in I$
>- $I$ is maximal iff for all ideals $J$ such that $I \subseteq J$ we have $I=J$ or $J=R$.

By [[Finite Integral Domains are Fields]], we get the following.
>[!lemma]
>If $I$ a **prime ideal** of $R$ such that $R /I$ is finite, then $I$ is a **Maximal Ideal**.

---
# References
