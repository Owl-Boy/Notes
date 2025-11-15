---
tags:
  - Note
---
202510041710

Tags : [[Parameterized Algorithms]]
# Kernelization Algorithm for Feedback Arc Set in Tournament
---
The **Feedback Arc Set in a Tournament** problem asks, given a [[Tournament]], does there exist a set $A$ of edges of size at most a given $k$ such that every directed cycle in the graph has an edge in $A$.

We consider the operation of reversing edges, that is, given a directed graph $G$ and a set of edges $F \subseteq E(G)$, we define the graph $G \circledast F$ to be the graph $G$ with the edges in $F$ reversed.

That is 
- $V(G*F)=V(G)$ and 
- $E(G*F)=E(G) - F +\text{rev}(F)$, 

where $\text{rev}(F)=\{ (b, a)\mid (a, b) \in F \}$

Thus we have the following lemma:
>[!lemma]
>If $G\circledast F$ is an acyclic tournament, then $F$ is a feedback arc set for $G$, and $F$ is an inclusion wise minimal feedback arc set iff $F$ is an inclusion wise minimal set such that $G\circledast F$ is acyclic.
>

That holds by contradiction, say there is a cycle in $G\circledast F$, then there must be a cycle that does not go over $F$.

That can be done by taking any cycle, if it has an intersection with $F$, then in the graph $G$, the cycle could have been taken along the other path on circle. This can be continued until all vertices of $F$ are avoided. 

Using this idea we will build a $k^2+2k$ kernel for the problem.
We get the following reduction:
- If an edge $e$ is in at least $k+1$ triangles, then reverse $e$ and reduce $k$ by $1$.
- If $v$ does not belong to any triangle, then delete $v$.

Now we show that every yes instance has at most $k(k+2)$ vertices.

Let $A$ be a feedback vertex set of the instance with reduction rules applied and exhausted. We have that every edge in $A$ has at most $k$ more vertices in a traingle with that edge, otherwise reduction rule 1 can be applied. We also know that all vertices are in a triangle, so this is an exhaustive set. So we are done.

---
# References
- [[Tournament]]