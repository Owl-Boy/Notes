---
tags:
  - Note
  - Incomplete
---
202501151501

Tags : [[Topics in Algorithms]]
# Fredmen and Tarjan's Algorithm
---
Fredman and Tarjan combined the ideas from [[Boruvka's Algorithm]] and [[Prim's Algorithm]] to construct an algorithm with running time $O(|E| \log ^* |V|)$ which is significantly better than the previous algorithms.

It tackles the problem of the heap operation by making sure that the neighbourhood of the heap remains bounded in size. It here uses the idea from Boruvka by making many such small trees and then collapsing them into vertices and repeating the process.

The Algorithm goes as follows:
1. Initially all vertices are unmarked.
2. While there exists an unmarked vertex, pick one and start prims algorithm on it, stop if
	1. The number of neighbours of the connected component crosses $t_{i}$ for some threshold, or
	2. Prim's algorithm connects to an already marked vertex.
	3. Then start it again from a new vertex
3. Once all vertices are marked, all connected trees are collapsed into vertices and we go back to step 1

---
## Correctness
#### Spanning tree
proof comes from that of Prims algorithm and of boruvka's algorithm. Each instance of prim's algorithm constructs a tree until it is stopped, or it connects to an existing tree, which also never creates a cycle. After collapsing, there are only edges drawn between 2 distinct connected components, so cycles are not possible. The algorithm ends when the entire graph is connected, hence makes a spanning tree.

#### Minimality
An edge is only added if it is a part of a minimum spanning tree: This comes from the idea of prims algorithm, which uses cut rule heavily.

---
## Complexity
The complexity of the algorithm depends on 2 things, how much work does each round take, and how many rounds are there.
- Each round takes $O(m_{i}+n_{i} \log t_{i})$ steps, so we can pick $t_{i}$ to be $2^{2m/n_{i}}$. Now each round takes $O(m)$ steps.
- Now we have to show that there are $\log^* n$ rounds. For this we need to show that $t_{i}$ increases exponentially at each step as if $t_{i} = 2^{t_{i-1}}$ then there can only be at most $\log^* n$ rounds.
	- For this we first claim that in any connected component $C$ at level $i$, $\sum_{v\in C} \deg(v) \geq t_{i}$.
	- With this we have  

$$
	  \begin{align} 
       \sum_{v\in V_{i}}\deg(v) &= 2m_{i} \\
\sum_{C\in V_{i}} \sum_{v \in C}\deg(v) &= 2m_{i} \\
n_{i+1} \cdot t_{i} &\leq 2m_{i} \\
t_{i} \leq \frac{2m_{i}}{n_{i+1}} &\leq \frac{2m}{n_{i+1}} = \log t_{i+1}
\end{align}
	  $$

---
# References
