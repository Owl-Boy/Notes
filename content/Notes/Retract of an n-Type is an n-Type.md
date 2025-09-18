---
tags:
  - Note
---
202508201508

Tags : [[Homotopy Type Theory]]
# Retract of an n-Type is an n-Type
---
>[!theorem]
>Let $p:X\to Y$ be a retraction and suppose that $X$ is an $n$-type. Then $Y$ must also be an $n$-type.

The proof is by induction on $n$ with base case $n=-2$.

Let $X$ be an $n+1$ type and let $s$ be a section of $p$ and let $\epsilon$ be the homotopy $p\circ s\sim{1}$. 

Since $X$ is an $n+1$-type we have that $s(y)=_{X}s(y')$ using $\text{ap}_{s}$ we now push it back to $Y$ so we get $p(s(y))=p(s(y'))$ and now we use the homotopy:
$$
\epsilon_{y}^{-1} \cdot p(s(r)) \cdot \epsilon_{y'}=r
$$
The claim is trivial for the base case and is handled in [[Some Contractible Types]].

>[!theorem] Corollary
>If $X\simeq Y$ and $X$ is an $n$-type then so is $Y$.

---
# References
- [[Contractible Types]]
- [[n-Types]]
- [[Some Contractible Types]]
- [[Retracts (HoTT)]]