---
tags:
  - Note
  - Incomplete
---
202501101601

Tags : [[Topics in Algorithms]]
# Properties of Minimum Spanning Trees
---
There are a couple of properties of minimum spanning trees that are very useful in constructing algorithms for these:

>[!theorem] Cycle Rule
>For any cycle $C$ which is a sub-graph of $G$, if $e$ is the edge with maximum weight in $C$ then no MST of $G$ will contain $e$.

Proof is easy, FTSOC assume there is an MST which contains $e$. Cut $e$ which is incident on $v_{1}$ and $v_{2}$.

Both $v_{1}$ and $v_{2}$ are in different connected components, and the rest of the cycle forms another path from $v_{1}$ to $v_{2}$ hence one of the edges most connect the two components which can be used to make the tree again. This will have a strictly smaller weight which is a contradiction.

>[!theorem] Cut Rule
>For any cut $C$ of the graph, the edge with the minimum weight exists in all MSTs.

FSTOC, assume there is an MST with a cut $C$ that violates the rule. Add the edge, this creates the cycle that crosses the cut. It must cross it an even number of times, so at least 2, so we can remove the non-minimal edge.

---
# References
