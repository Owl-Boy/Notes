---
tags:
  - Note
  - Incomplete
---
202502181502

Tags : [[Verification of MST]], [[Topics in Algorithms]]
# Tree Path Maxima Problem
---
>[!question]
>Given a tree $T$ with real edge weights and a list of pairs of distinct nodes in $T$, determine for each pair $(u, v)$ on the list, a heaviest path edge on the path from $u$ to $v$ in $T$.

^c0687a

---
## Reduction from MST Verification
There is a straightforward reduction from this problem to verification of [[Minimum Spanning Trees]]:
- Given a tree $T$, we want to check if this is a minimum spanning tree:
- We construct the Tree Path Maxima Problem with inputs $T$ and pairs $u, v$ forall $(u,v) : E$.
- Now for any pair $u, v$ If we have that the output of the tree path maxima problem on that pair returns an edge of weight larger than the edge that directly connects $u, v$ then the tree is not an [[Minimum Spanning Trees|MST]], otherwise it is.
This reduction takes linear time: $O(|E|)$.

---
# References
[[Special Case of Tree Path Maxima Problem]]