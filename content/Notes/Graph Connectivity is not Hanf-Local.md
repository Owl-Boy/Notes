---
tags:
  - Note
  - Incomplete
---
202501191601

Tags : [[Finite Model Theory]]
# Graph Connectivity is not Hanf-Local
---
***FTSOC***, assume graph connectivity is [[Hanf-Locality|Hanf-local]], and $\text{hlr}(Q)=d$. Let $m >2d+1$ and choose 2 graphs $G_{m}^1$ and $G_{m}^2$ as shown in the figure.
![[Pasted image 20250119163414.png|500]]

Their set of nodes have the same cardinality, so let $f$ be a bijection between the set of nodes of each graphs.

Since the length of each cycle $> 2d+1$, the $d$-[[Neighborhood (Finite Model Theory)|neighborhood]] of any node $a$ is isomorphic: a chain of length $2d+1$ with $a$ in the middle. Hence $G^1_{m}\leftrightarrows_{d} G^2_{m}$, and they must agree on $Q$. But $G^2_{m}$ is connected, and $G_{m}^1$ is not. Thus graph connectivity is not Hanf-local.

---
# References
