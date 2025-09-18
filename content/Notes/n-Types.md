---
tags:
  - Note
---
202508201508

Tags : [[Homotopy Type Theory]]
# $n$-Types
---
$n$-Types are homotopy type theory analogues of $n$-truncated spaces from homotopy theory, these are types with no non-trivial homotopy structure above level $n$, we define these using the following:
>[!definition]
>The predicate $\text{is-n-type}:\cal U\to U$ is defined as follows for all $n\geq {2}$:
>$$
>\text{is-n-type}(X):\equiv
>\begin{cases}
>\text{is-Contr}(X) & \text{if }n=-2\\
>\prod_{(x,y:X)}\text{is-n'-type}(x=_{X}y) & \text{if }n=n'+1
\end{cases} 
>$$

we say $X$ is an $n$-type if $\text{is-n-type}(X)$ is inhabited.

---
# References
- [[Contractible Types]]