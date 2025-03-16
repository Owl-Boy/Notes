---
tags:
  - Note
---
202503081503

Tags : [[Logic]], [[Finite Model Theory]]
# Ranked Trees in Logic
---
A **Ranked Tree** is a tree where the number of children of each non-leaf node is the same (or is bounded above by a fixed value $k$).

Here the value $k$ will be fixed to be $2$ but the same can be done for any $k \in \mathbb{N}$.

Each node now can be represented by a graph by a string in $(0\mid 1)^*$.

>[!definition]
>A *Tree Domain* describes the set of strings that represent nodes of a tree. Such a set $D$ is a prefix closed subset of $(0 \mid 1)^*$ and if $s\in D$ then either both $s 1$ and $s 0$ are in $D$ or neither of them are in $D$
>
>A $\Sigma$-tree is defined as a tuple $(D, f)$ where $D$ is a tree-domain and $f: D \to \Sigma$ is a labelling function.

We represent such a tree as a first order structure as follows:
$$
M_{T} = \langle D, \prec, (P_{a})_{a\in \Sigma}, \text{succ}_{1}, \text{succ}_{2}\rangle
$$

>[!definition]
>The set of trees that can be represented by a formula $\Phi$ for some logic is the set of tree that satisfy the formula
>$$
>L_{T}(\Phi) = \{ T\in \text{Tree}(\Sigma) \mid M_{T} \vDash \Phi  \}
>$$

---
# References
