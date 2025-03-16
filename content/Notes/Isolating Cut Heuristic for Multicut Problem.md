---
tags:
  - Note
  - Incomplete
---
202503091503

Tags : [[Topics in Algorithms]]
# Isolating Cut Heuristic for Multicut Problem
---
The [[Multi-way Cuts]] problem asks for a cut that separates every vertex from every other vertex in a subset $S$ of the vertices.

One greedy idea behind solving the problem is for each $s\in S$, find an *isolating cut*, which is a cut that separates $s$ from every other vertex in $S$. This can be found using the following algorithm:
- Create a new vertex $t$ and connect every vertex in $S \setminus \{ s \}$ to $t$ with edges of $\infty$ weights.
- Find an $s-t$ mincut.

To construct a multiway cut solution from that. Construct an *isolating cut* for each $s\in S$ and take the union of the lightest $k-1$ such cuts.

>[!theorem] 
>The Isolating Cuts Heuristic Algorithm has an approximation ratio of $2-\frac{2}{k}$.

***Proof:*** 
Assume $E^*$ is the optimal solution for the problem. This solution divides the graph into $k:= |S|$ connected components. Let $E_{i}^*$ be the set of edges that disconnect the $V_{i}$ component from the others.

We have the isolating cut $wt(E_{i})\leq \delta(V_{i})$ where $\delta(V_{i})$ is the set of edges going out of $V_{i}$. We also have that $2 \cdot wt(E^*) = \delta(V_{1}) + \dots \delta(V_{k})$.

So we have that $wt(E_{1})+ wt(E_{2})\dots wt(E_{k})<2 \cdot wt(E^*)$.

Since we are removing the heaviest cut to get the answer we get:
$$
wt(E_{1}) + wt(E_{2})\dots wt(E_{k-1}) \leq 2-\frac{2}{k} wt(E*)
$$

The following is a tight example:
![[Pasted image 20250309160237.png]]

---
# References
