---
tags:
  - Note
  - Incomplete
---
202501101701

Tags : [[Topics in Algorithms]]
# Prim's Algorithm
---
Prim's Algorithm finds the [[Minimum Spanning Trees]] by starting with a vertex, and starting to build a tree from it as a seed, where in each step 1 vertex that is not already a part of the tree is added to it. 

The algorithm goes as follows

>[!todo] TODO: Pseudo Code

The Algorithm heavily depends on the complexity of the 
- insert
- modify
- get_min
functions, and different implementations of priority queues would give different complexities of the algorithm. The one that is generally used for best case complexity is [[Fibonacci Heap]].

---
## Correctness
#### Spanning tree:
The algorithm on each step adds a vertex while maintaining the tree structure, hence, after adding all vertices, one gets a spanning tree.

#### Minimality:
This algorithm uses the cut rule in every step, where the 2 cuts are the tree that has been constructed yet, and the rest of the scattered nodes. Hence it leads to a minimum spanning tree.

---
# References
[[Kruskal's Algorithm]]