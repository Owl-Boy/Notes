---
tags:
  - Note
---
202510102310

Tags : [[Graph Theory]]
# Crown Lemma
---
>[!theorem]
>Let $G$ be a graph without isolated vertices and with at least $3k+1$ vertices. Then there is a polynomial time algorithm that either 
>- Finds a matching of size $k+{1}$ in $G$ or,
>- Finds a crown decomposition of $G$.

We first find an inclusion maximal matching $M$ in $G$. If the size of the maximum matching is at least $k+1$ then we are done. 

Otherwise, let $V_{M}$ be the end points of $M$. We have that $V_{M}$ has size at most $2k$. 
Consider the set $I=G(V)-V_{M}$. This is an independent set as $M$ is a maximal matching. 

Consider the bipartite graph $G_{I, V_{M}}$, which is the bipartite graph between $I$ and $V_{M}$. Let $X$ be the minimum vertex cover and $M'$ be the maximum sized vertex cover which can be found in polynomial time using [[Hall's Marriage Problem]]. If $M'$ is more than $k$ we are done, so we assume $|M'| \leq k$. 

We have that either $X$ intersects $V_{M}$ or $X=I$. This is if $I$ is not in the set $X$, at least one of its neighbors are in the set, which are all in $V_{M}$ as $I$ is an independent set. But if $X=I$ then $|X|\leq k$, thus $|I|+|V_{M}| \leq 3k$ which is a contradiction.

Thus $X$ nontrivially intersects $V_{M}$, Now we will construct the crown decomposition. Let $M^*$ be the set of edges with exactly 1 end-point in $X$. Let $H=X\cap V_{M}=X\cap V_{M^*}$ The crown $C=V_{M^*}\cap I$, and the remaining part is $R$.
$C$ is the set of end points of a matching, so is trivially independent and the matching $M^*$ is the matching between elements.

>[!note]
>The rough overview of the idea was that, take a graph, and then a maximal matching to get an independent set $I$, let the rest of the vertices be $V'$.
>
>If we look at the pair of vertices $I$ and $V'$, we can find a maximum matching $M'$, which is also the vertex cover between them (ignoring the vertices inside $V'$, by [[Konigs Theorem]]). The edges of $M'$ that cover all other edges between $I,V'$ form the crown, the end points in $V'$ form the head, the one in $I$ from the crown

---
# References
- [[Hall's Marriage Problem]]
- [[Crown Decomposition]]
- [[Konigs Theorem]]
- [[Hopcroft-Karp Algorithm]]