---
tags:
  - Note
  - Incomplete
---
202502100102

Tags : [[Topics in Algorithms]]
# Tree Packing
---
>[!question]
>The *Tree Packing* problem asks: Given a graph $G$, what is the maximum size of a set of edge-disjoint spanning tree.

Lets look at a bunch of straightforward observations first:
- If a vertex has degree $n$, then there cannot be more than $n$ vertex disjoint spanning trees.

This is a nice bound, but by looking at cuts, this can be made better
- Given any cut, if $n$ is the number of edges across the cut, then there can be at most $n$ disjoint spanning tree.
- The previous example was a special case where one of the partitions is a singleton.

A tighter bound, which will be the one that will be used is
- Given any partition, let $m$ be the number of parts and let $n$ be the number of edges across partitions, then the number of possible disjoint spanning trees are at most $\frac{n}{m-1}$.
- The previous bound was a special case of this when the partition is a double-ton set.

Turns out, the final bound happens to be a tight lower bound:

>[!theorem] Theorem: Tutte-Nash-Williams
>The maximum number of edge-disjoint spanning trees in a graph $G$ is given by:
>$$
>\tau(G) = \left\lfloor  \min_{P} \frac{|E_{P}|}{|P|-1}  \right\rfloor 
>$$

A weaker version of the theorem is discussed in [[Fractional Tree Packing]].

---
# References
