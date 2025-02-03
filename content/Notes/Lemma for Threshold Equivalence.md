---
tags:
  - Note
---
202502020502

Tags : [[Finite Model Theory]]
# Lemma for Threshold Equivalence
---
>[!theorem] 
>For each $k, l>0$  there exists $d, m> 0$ such that for $\mathfrak{A, B}\in \text{STRUCT}_{l}[\sigma]$:
>$$
> \mathfrak A\leftrightarrows^\text{thr}_{d, m} \mathfrak B \quad \text{implies} \quad \mathfrak A \equiv_{k} \mathfrak B
>$$

We first inductively define $r_{0}=0$ and $r_{k+1}=3 \cdot r_{k}+1$ and the prove that duplicator can play the [[Ehrenfeucht-Fraïssé Game|EF Game]] on $\frak A, B$ in such a way that after $i$ rounds

$$
N_{r_{k-i}}^\mathfrak A(\vec{a_{i}}) \cong N_{r_{k-i}}^\mathfrak B(\vec{b_{i}})
$$
where $\vec{a_{i}}$ and $\vec{b_{i}}$ are the moves played on the 2 arenas until the $i^\text{th}$ move.

We shall take $d=r_{k-1}$ and now we only have to specify $m$. The idea comes form [[Gaifman-Locality implies BNDP]], where we constructed the function $G_{\sigma}$ which gives the maximum size of a ball of $d$ radius. So we set $m=k \cdot G_{\sigma}(r_{k}, l)$.

Now we just need to prove that these values work by induction.
Suppose the equivalence holds until the $i^\text{th}$ round, then we have $N_{3r+1}^\mathfrak A(\vec{a}_{i}) \cong N_{3r+1}^\mathfrak B(\vec{b}_{i})$, where $r=r_{k-(i-1)}$. Suppose in the $i+1^\text{th}$ round the spoiler plays $a\in A$,
- If $a\in B_{2r+1}^\mathfrak A(\vec{a}_{i})$, then the isomorphism between $B_{3r+1}^\mathfrak A(\vec{a})$ and $B_{3r+1}^\mathfrak B(\vec{b})$ gives the corresponding $b$.
- Otherwise let $\tau$ be the isomorphism type of the $r$-neighborhood of $a$, we need to find an element $b$ in $B$ with the same isomorphism type and $d_{\mathfrak B}(\vec{b}, b) >2r+1$, then the duplicator can pick that element. There must be such a point because $2r+1<r_{k}$, and $|\vec{b}|$ has at most $k$ points in it. So the number of points in the neighbourhood are bounded and there will always by $k \cdot G_{\sigma}(2r+1,l)$ which is less than $m$.

---
# References
