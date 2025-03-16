---
tags:
  - Note
---
202503141903

Tags : [[Finite Model Theory]], [[Logic]]
# Unranked Trees in Logic
---
An **Unranked Tree** is a tree where each node can have different finite number of children.

>[!definition]
>A *Tree Domain* is a subset $D$ of $\mathbb{N}^*$ which is prefix closed such that for each $s \cdot i \in D$ we have $s \cdot j\in D$ for all $i\leq j$.
>
>A $\Sigma$-tree is defined as a tuple $(D, f)$ where $D$ is a tree-domain and $f: D\to \Sigma$ is a labelling function.

Unliked [[Ranked Trees in Logic|Ranked Trees]] it is no longer sufficient to have 2 successor relations as there are arbitrarily many children for each node, so we add further structure on to the tree.
$$
M_{T} = \langle D, \prec , (P_{a})_{a\in \Sigma}, <_{\text{sibl}} \rangle 
$$

The structure added here is that there is an order relation on the sibling.

>[!definition]
>The set of trees that can be represented by a formula $\Phi$ for some logic is the set of trees that satisfy the formula
>$$
>L_{T}(\Phi) = \{ T \in \text{Treesq}(\Sigma) \mid M_{T} \vDash \Phi\}
>$$

---
# References
