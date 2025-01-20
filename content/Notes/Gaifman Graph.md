---
tags:
  - Note
  - Incomplete
---
202501191301

Tags : [[Finite Model Theory]]
# Gaifman Graph
---
Assuming a purely relational signature.
>[!definition]
>Given a $\sigma$-structure $\mathfrak A$, its *Gaifman Graph*, denoted by $\mathcal G(\mathfrak A)$ is defined as follows:
>- The set of nodes of $\mathcal G(\mathfrak A)$ is $A$.
>- There is an edge between $a_{1}, a_{2}\in A$ if
>	- $a_{1} = a_{2}$ or,
>	- there is a relation $R$ in $\sigma$ such that for some tuple in $R^\mathfrak A$, both $a_{1}$ and $a_{2}$ occur in $t$.

Note that $\mathcal G(\mathfrak A)$. If $\frak A$ is already an undirected graph, then $\mathcal G(\mathfrak A)$ adds the diagonal $\{ (a, a) : a \in A \}$ to the graph. If $\mathfrak A$ is a directed graph, then $\mathcal G(\mathfrak A)$ forgets the directions and adds the diagonal. 

---
# References
- [[Neighborhood (Finite Model Theory)]]