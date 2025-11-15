---
tags:
  - Note
  - Incomplete
---
202510121910

Tags : [[Graph Theory]]
# Expansion Lemma
---
>[!Theorem]
>Let $q\geq {1}$ be a positive integer, and $G$ be a bipartite graph with paths $A, B$ such that
>- $|B|\geq q|A|$
>- There is no isolated vertex in $B$.
>
>Then there are non empty sets $X \subseteq A$ and $Y \subseteq B$ such that
>- There is a $q$-expansion of $X$ into $Y$
>- No vertex of $Y$ has a neighbour outside $X$
>
>And these sets can be found in polytime.

Note that $X, Y$ and the rest of the graph from a [[Crown Decomposition]] of the graph. 

The construction is by recursion, and it trivially holds for the base case when $|A|=1$.

We use [[Extended Hall's Lemma]], if $A$ has a q-expansion into $B$, then we can use that. Otherwise we can find a subset $Z$ of $A$ in polytime such that $|N(Z)|<q|Z|$. We can construct a graph $G'$ by removing $Z$ and $N(Z)$ from $G$. We still have that all properties of the problem hold for $G'$. We keep doing this recursively and we are guaranteed to stop when $G'$ is a singleton.



---
# References
- [[Extended Hall's Lemma]]
- [[Crown Decomposition]]