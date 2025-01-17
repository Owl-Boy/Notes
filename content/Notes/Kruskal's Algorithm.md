---
tags:
  - Note
---
202501101701

Tags : [[Topics in Algorithms]]
# Kruskal's Algorithm
---
Kruskal's Algorithm find a [[Minimum Spanning Trees]] for an undirected edge-weighted graph. It is a greedy algorithm that in each step, adds the lightest edge which does not create a cycle in a graph to the tree.

The algorithm goes as follows

```rust
fn Kruskal(G) {
  for v in G.V { make_set(v); }
  sort(G.E) // by weight
  for (u, v) in G.E {
    if find_set(u) != find_set(v) {
      F := F.add(u, v);
      union(find_set(u), find_set(v));  
    }
  }
}
```

The [[Union Find]] data structure is used to efficiently locate cycles, hence most of the cost of running the algorithm is done on line $3$ for sorting the weights.

---
## Correctness
#### Spanning tree:
If an edge is not already added by the algorithm, then it will create a cycle, hence the graph must be connected and not have cycles: aka a tree.

#### Minimality:
This algorithm uses the cut rule in every step. In any cut, the smallest weight is always looked at first since weights are ordred, hence the cut rule is always preserved.

---
# References
[[Prim's Algorithm]]