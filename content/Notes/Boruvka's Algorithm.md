---
tags:
  - Note
---
202501151501

Tags : [[Topics in Algorithms]]
# Boruvka's Algorithm
---
Boruvka's Algorithm find the [[Minimum Spanning Trees|Minimum Spanning Tree]] using the following property.

>[!theorem]
>Given any vertex, its edge with minimum weight incident upon it will be in the minimum spanning tree.

The algorithm starts by adding all minimum weight edges for each vertex, and then it collapses all components as vertices and repeats till the graph gets connected.

The Algorithm goes as follows:
```
T = []
while |V| > 1:
	for v in V:
		e = edge incident on v with minimum weight
		T.add(e)
	replace vertices with components
	remove edges within component
```

The complexity of the algorithm is $O(|E| \log |V|)$ as each time at most all edges will be checked, and each time, the number of connected components go down by half, so the algorithm has at most $\log |V|$ rounds.

---
### Correctness
#### Spanning Tree:
In each step, if the components themselves are tree and the graph connecting the components are also trees then there are no cycles. 
So we just need to show that the graph connecting the components does not form a cycle. 
FTSOC, it does. Then consider a cycle with vertices $a_{1}\dots a_{n}$. without loss of generality assume $a_{1}, a_{2}$ is in the graph because of $a_{1}$. That would mean that weight of $a_{1}, a_{n}$ is more and is in the graph because of $a_{n}$. That would mean that $a_{n}, a_{n-1}$ has even more weight and is because of $a_{n-1}$ and the chain goes on till we get weight of $a_{1}, a_{2}$ is more than $a_{1},a_{2}$.

#### Minimality
The algorithm uses cut rule whenever it adds an edge, consider the cut containing only a connected algorithm and nothing else, then  it pics the smallest weight edge each time.

---
# References
