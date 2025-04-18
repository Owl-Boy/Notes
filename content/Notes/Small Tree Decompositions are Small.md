---
tags:
  - Example
---

202503311638

tags : [[Finite Model Theory]]

#  Small Tree Decompositions are Small
---
>[!theorem]
>Given any small decomposition $\cal T$ of a graph $\mathcal G$, we have $|T| \leq |G|$. Further, every tree decomposition can be converted to a small decomposition in linear time.

The proof is nice, we can claim that each leaf's bag has a vertex of $G$ such that no other node of the tree contains that vertex. That is because all  vertices of $\cal G$ that are in a leaf and in another node of $\cal T$ are also in the parent of the leaf.

Now we ignore the leaves and the vertex unique to them and make the same argument for the parents of the leaves. Hence there are at most as many nodes as there are vertices in $\cal G$.

To convert a tree decomposition to a small tree decomposition, starting from the leaves, move upwards and for each pair $u-v$ such that $B_{u} \subseteq B_{v}$ or $B_{v} \subseteq B_{u}$, merge to 2 vertices together.


---
# Related
