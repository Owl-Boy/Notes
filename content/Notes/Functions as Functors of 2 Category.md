---
tags:
  - Note
  - Incomplete
---
202507131807

Tags : [[Homotopy Type Theory]]
# Functions as Functors of 2 Category
---
We know that [[Types are Higher Groupoids]] and that [[Functions as Functors|functions are functors]], but we have only seen the categorical behaviour has 1-category. We have the following extension to a theorem we have done previously:

>[!theorem]
>Given $f:A\to B$ and $x,y:A$ and $p,q:x=y$ and $r:p=q$, we have a path $\text{ap}^2(r):f(p)=f(q)$.

The proof is just path induction on $r$.

There is also the dependent version of this:
>[!lemma]
>Given $P:A\to \cal U$  and $x, y:A$ and $p,q:x=y$ and $r:p=q$, for any $u:P(x)$ we have $\text{transport}^2(r, u):p_{*}(u)=q_{*}(u)$.

Proof again is by path induction.

To finally state the definition, note that we need to write about an equality between dependent paths, so given $x,y:A$ and $p,q:x=y$ and $r:p=q$ and also points $u:P(x)$ and $v:P(y)$ and dependent paths $h:u=_{p}^Pv$ and $k:u=_{q}^Pv$. By our definition of dependent paths, this means $h:p_{*}(u)=v$ and $k:q_{*}(u)=v$, so we can define the dependent 2-path to be
$$
(h=_{r}^Pk):\equiv h=\text{transport}^2(r,u)\cdot k
$$
so intuitively, we have a path from $p_{*}(u)$ to $v$ and a path from $q_{*}(u)$ to $v$, and a path from $p_{*}(u)$ to $q_{*}(u)$. We state the first 2 paths to be the same if going from $p_{*}(u)$ to $v$ directly is equal to taking a detour from $q_{*}(u)$.

>[!theorem]
>Given $P:A\to\cal U$ and $x,y:A$ and $p,q:x=y$ and $r:p=q$ and a function $f:\prod_{x:A}P(x)$, we have $\text{apd}^2(r):\text{apd}_{f}(p)=_{r}^P\text{apd}_{f}(q)$.

proof again is path induction.


---
# References
- [[2-Categories]]