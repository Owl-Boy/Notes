---
tags:
  - Note
---
202501230401

Tags : [[Complexity Theory]], [[Topics in Algorithms]]
# Steiner Trees are NP Complete
---
The decision problem for Steiner Trees is the following:
>[!question]
>Given a graph $G$ and a weight $d$, is there a Steiner Tree of weight $\leq d$ in the graph.

The problem is clearly in $NP$ as given a graph, it is very easy to check if its weight is less than $d$ and it covers all the necessary vertices.

---
## Reduction

The proof for it being $\text{NP-HARD}$ is a reduction from [[Exact 3 Cover]] as follows:

Given a set $X$, st $|X| = p$ and set of 3-size subsets $C = \{ C_{1}, C_{2}\dots C_{n} \}$, one can construct the following graph:
- Let $V = \{  v \} \cup X \cup C$
- Let $E$ contain the following edges:
	- For each $i \in [1..n]$ there is an edge $(v, C_{i})$
	- If $x_{j}\in C_{i}$ for some $i, j$ then add the edge $(x_{j}, C_{i})$

Then there exists an exact 3 set cover of $X$ using $C$ iff the graph $G= (V, E)$ as a steiner tree of weight $4p$, where $K= \{ v \} \cup X$.

---
## Proof
Left to right is easy, the solution to the Exact 3 cover gives us exactly the set of steiner vertices that are to be selected, namely the subset of $C$ which was the solution.

For the other direction, consider a steiner tree of size at most $4p$, this means that the tree contains $4p+1$ vertices, 3p of them are in the bottom layer, and one is in the top layer. This means that there are exactly $p$ elements from the second layer. By construction, each element in $p$ as at most 3 children in any tree, and by php, there would have to be eactly $3$, The set chosen here in the second layer is the solution to the Exact 3 Cover.
 
---
# References
