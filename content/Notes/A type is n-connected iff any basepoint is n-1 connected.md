---
tags:
  - Note
---
202509242209

Tags : [[Homotopy Type Theory]]
# A type is $n$-connected iff any basepoint is $(n-1)$-connected
---
>[!theorem]
>Let $A$ be a type and $a_{0}:\mathbf{1}\to A$ a basepoint, with $n\geq -1$. Then $A$ is $n$-connected iff the map $a_{0}$ is $(n-1)$-connected.

First, assume that $a_{0}$ is $(n-1)$ connected, we will use the corollary in [[Characterizing n connectedness using n-types]]. We already have that the map $\lambda b.(\lambda a.b):B\to(A\to B)$ has a retraction, given by $f \mapsto f(a_{0})$, now we need to show that it also has a section. So we need to show that for each function $f$, there is a $b:B$ such that $f=\lambda a.b$. We define $b:\equiv f(a_{0})$, Now we need to find a proof for the statement $P(a):\equiv f(a)=f(a_{0})$. We have that $P$ is a family of $n-1$ types and we have $P(a_{0})$. This we have $\prod_{(a:A)}P(a)$ as $a_{0}:\mathbf{1}\to A$ is $(n-1)$ connected, hence we are done.

For the other side, assume $A$ is $n$-connected. Let $P:A\to (n-1)\!-\!\text{types}$ be a type family and we have $u:P(a_{0})$. It will suffice to construct $f:\prod_{a:A}P(a)$ such that $f(a_{0})=u$. Not that $(n-1)\!-\!\text{types}$ is an $n$-type, thus by the corollary in [[Characterizing n connectedness using n-types]], there is an $n$-type $B$ such that $P=\lambda a.B$. This we have a family of equivalences $g:\prod_{a:A}(P(a)\simeq B)$. Define $f(a):\equiv g_{a}^{-1}\circ g_{a}(u)$, then we are done.

---
# References
- [[Characterizing n connectedness using n-types]]