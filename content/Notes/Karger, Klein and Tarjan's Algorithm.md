---
tags:
  - Note
  - Incomplete
---
202501172101

Tags : [[Topics in Algorithms]]
# Karger, Klein and Tarjan's Algorithm
---
This Algorithm is a [[Randomized Algorithms]], that returns the [[Minimum Spanning Trees]] in time randomized $O(|E|)$. This algorithm is a [[Randomized Algorithms#^1314ea|Las Vegas Algorithm]], which means it always returns the minimum spanning tree, but the runtime is a random variable. The above bound is on the average runtime.

>[!note]
>The bound can also be given to running time with a high probability, but I have not checked the proof.

The idea behind the algorithm
- It does boruvka for a couple of steps. 
- Then it deletes half the edges (randomly) and finds a good enough minimum spanning tree for that
- Using that it removes most of the bad edges and repeats the process until the minimum spanning tree is formed.

This algorithm relies on a key ideas:
- Given a forest $F$, an edge $e$ is called $F$-heavy if adding it to $F$ creates a cycle with $e$ as its largest weighted edge. By cycle rule we get that an MST will have no e-weight edges. All other edges are called $F$-light edges.
- The above idea is not trivial to implement, there is an algorithm by [[Komlos's Algorithm|Komlos]] which is deterministic and finds all the $F$-light edges in $O(|E|)$ time. The algorithm shall use that.

---
## The Algorithm:

KKT($G = (V, E)$):
1. Given graph $G= (V, E)$ run [[Boruvka's Algorithm]] on it 3 times. If this graph is a tree then we just return it, otherwise we shrink the connected components to get $G' = (V', E')$.
2. Now we go to each edge in $E'$ and put it in $E_{1}$ with probability $\frac{1}{2}$.
3. Then we recursively find $F_{1}= \text{KKT}(V', E_{1})$
4. Let $E_{2}$ be all the $F_{1}$-light edges of $E'$. This step uses [[Komlos's Algorithm]].
5. Now with a lot of bad edges deleted, we start the process again with the recursive call $F_{2} = \text{KKT}(V', E_{2})$
6. Then we return $F_{2}$ along with the edges in step 1.

---
## Correctness 
The algorithm only includes edges as dictated by [[Boruvka's Algorithm]], and it only removes edges that are guaranteed to not be in the tree by the cycle rule.

The [[Complexity of KKT Algorithm]] is discussed here.

---
# References
- [[Randomized Algorithms]]
- [[Boruvka's Algorithm]]
- [[Komlos's Algorithm]]