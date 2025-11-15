---
tags:
  - Note
---
202510121810

Tags : [[Graph Theory]]
# Extended Hall's Lemma
---
>[!definition]
>A *q-star* is a graph with $q+1$ vertices, with one vertex called the center, and the only edges are from the center to every other vertex.
>
>An extension of that idea is called a $q$-expansion. Given a bi-partite graph with parts $A$ and $B$, a *q-expansion* of $A$ is a subset of edges that from a disjoint union of *q-star* from each vertex in $A$.

![[Pasted image 20251012185213.png]]

>[!lemma]
>Let $G$ be a bipartite graph with parts $A$ and $B$. Then there is a $q$-expansion from $A$ to $B$ iff $|N(X)|\geq q|X|$ for every $X \subseteq A$. Furthermore, if there is no $q$-expansion from $A$ to $B$, then a set $X \subseteq A$ with $|N(x)|<q|X|$ can be found in polynomial time.

If $A$ has a $q$-expansion, then the statement trivially holds.

For the opposite direction, construct a new bi-partite graph with partitions $(A',B)$ where $A'$ consists of $q$ copies of $A$, and each copy has the same neighbourhood as the original. 

We would like to prove that there is a matching from $A'$ to $B$. If a matching exists, it will give us an expansion, we will get a q-extension of $A$ by quotienting all the copies together. And if a $q$-extension exists from $A$ to $B$ then $A'$ can be given a matching trivially.

Thus we use the condition from [[Hall's Marriage Problem]]. Otherwise, Hall's theorem gives us a subsets $X$ such that $|N_{G'}(X)|<|X|$. If $X$ contains a copy of a vertex $v$, then it contains all copies of the vertex $v$, as adding them will not change $N_{G'}(X)$ but will increase $X$. Thus quotienting all copies together gives us a set of size $\frac{|X|}{q}$, which satisfies our claim.


---
# References
[[Expansion Lemma]]