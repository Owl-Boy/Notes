---
tags:
  - Note
  - Incomplete
---
202509301509

Tags : [[Games on Graphs]], [[Parity Games are solvable in Qusaipolynomial time - introduction]]
# Reachability Automata for Parity Games
---
Let $\cal G$ be a parity game and let $\cal D$ be a deterministic reachability automata over the alphabet
$$
(\{ 1\dots n \}\times \{ 1\dots d \})^\omega
$$
such that words where are loops are even are accepted and words where all loops are odd are rejected.

![[Pasted image 20251003053635.png]]

where $n$ is the number of states in $\cal G$ and $d$ is the largest priority seen on any edge in $\cal G$. Then:

>[!theorem]
>The parity game $\cal G$ can be solved in time:
>$$
>O((\text{number of edges in }\mathcal G)\times(\text{number of states in }\mathcal D)) + \text{time to compute }\cal D
>$$

The first step is to construct the game $\cal G \times D$ which cam be done in the time required. Now we need to show that player $0$ wins the game $\cal G$ iff they win the game $\cal G \times D$. 

To show this, consider that player $0$ has a winning strategy in game $\cal G$. Since Parity games have memoryless determinacy, Consider the subgraph $G_{0}$ of the game $\cal G$ that is found by restricting to set of edges to those suggested by a memoryless winning strategy. Following this path on the game $\cal G \times D$ will guarantee that all words have only even cycles, thus all words corresponding to games won by player $0$ are accepted. By symmetry, this also holds for player $1$.

Since $\cal G \times D$ is positional game, it is possible to solve it in linear time in terms of number of edges, which satisfies the requirement.

The following construction of $\cal D$ shows that it is possible to get the time complexity as given in [[Parity Games are solvable in Qusaipolynomial time - introduction]]:
- [[Succinct Reachability Automata for Parity Games]]

---
# References
- [[Parity Games are solvable in Qusaipolynomial time - introduction]]
- [[Succinct Reachability Automata for Parity Games]]