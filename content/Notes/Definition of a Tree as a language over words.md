---
tags:
  - Note
  - Incomplete
---
202511162211

Tags : [[Games on Graphs]]
# Definition of a Tree as a language over words
---
A (rooted) tree is a collection of nodes, and one of the properties of a tree is that, given a fixed vertex (root), every vertex has a unique path from the root. 

The simplest non-trivial case is that of a binary tree, where we can think of each vertex has having at most 1 left neighbour and at most 1 right neighbour (we distinguish between left and right child even if there is just one of them as that is closer to how it is represented in programs). Then each vertex can be through of as a sequence of _left_ and _right_ steps that it takes to get to it from the root.

Similarly , we can fix the maximum number of children of each node by $k$, thus for each edge from a vertex that goes to its child, we can give a unique number less than $k$ to every such edge. We can now represent each vertex as a path which is an element of $[k]^*$.

This definition is formalised as follows:
>[!definition]
>Given a set of direction $D$, a **$D$-tree** is a set $T \subseteq [D]$ such that if $(x::xs) : T$ then we have that $xs : T$.

>[!attention] Notation : [[Words are lists of letters]]

Here each element can be through of as a path on top of the empty list $\square$, which corresponds to the root, and the condition says that if a non-root-vertex belongs to the tree, then so does its parent. 

Any list $xs:T$ such that $x::xs$ is not in $T$ is called a leaf.

>[!definition]
>Given a set of direction $D$ and a let of labels $\Sigma$, a **$\Sigma$-labelled $D$-tree** is given by
>$$
>\mathcal T = (T, \tau)
>$$
>where $T$ is a $D$-tree and $\tau:T \to \Sigma$ is a labelling function.
 
---
# References
- [[Words are lists of letters]]
- [[Alternating Tree Automata]]