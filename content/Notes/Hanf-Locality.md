---
tags:
  - Note
---
202501191601

Tags : [[Finite Model Theory]]
# Hanf-Locality
---
>[!definition]
>An $m$-query $Q$ on a $\sigma$-structure is *Hanf-local* if there exists a number $d \geq 0$ such that for every structure $\mathfrak {A, B}\in \text{STRUCT}[\sigma], a\in A^m,b\in B^m$,
>$$(\mathfrak A, \vec{a})\leftrightarrows_{d}(\mathfrak B, \vec{b}) \implies (\vec{a}\in Q(\mathfrak A) \iff \vec{b} \in Q(\mathfrak B))$$

The smallest $d$ for which the above condition holds is called the *Hanf-locality* rank of $Q$ and is denoted by $\text{hlr}(Q)$.

>[!tip] Intuition
>The intuitive idea behind this seems to be that, the $\leftrightarrows_{d}$ shows that up to some distance $d$, the neighbourhoods of $\vec{a}$ along with any other element is identical to $\vec{b}$ and another element. Hence making the graphs locally similar. So the query respecting that local equivalence would be special and we would like to talk about it.

*Hanf-locality* is most commonly used for Boolean queries; then the definition says that for some $d\geq 0$ for every $\mathfrak {A, B} \in \text{STRUCT}[\sigma]$, the condition $\mathfrak A \leftrightarrows_{d} \mathfrak B$ implies that $\mathfrak A$ and $\mathfrak B$ agree on $Q$.

The way to use *Hanf-locality* to show that a query $Q$ is not definable in a logic $\cal L$ is:
- Show that every $\cal L$ query is *Hanf-local*, and
- Show that $Q$ is not *Hanf-local*.

The canonical example of the above is [[Graph Connectivity is not Hanf-Local]].

---
# References
