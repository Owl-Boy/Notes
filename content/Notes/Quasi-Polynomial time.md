---
tags:
  - Note
---
202509301509

Tags : [[Complexity Theory]]
# Quasi-Polynomial time
---
>[!note]
>This is the class of decision problem that can be decided by a [[Turing Machines|Determinisitic Turing Machine]]

This is defined to be the class of problems that can be solved in roughly $2^{O((\log\ n)^c)}$ time, formally

$$
\mathbf{QP}:\equiv \bigcup_{c:\mathbb{N}}\mathbf{Dtime}\left( 2^{O((\log\ n)^c)} \right) 
$$
These problems are considered to be candidates for [[NP (Complexity Class)|NP Intermediate]] problems, as they are not [[P (Complexity Class)|PTime]] and are unlikely to be [[NP Complete]].

## Examples
- [[Parity Games are solvable in Qusaipolynomial time - introduction]]
- Finding the smallest dominating set in a tournament
- Finding a graph with fewest vertices that is not an induced sub-graph of a given graph.

---
# References
- [[Complexity Classes]]
- [[Turing Machines]]
- [[NP (Complexity Class)]]
- [[NP Complete]]
- [[P (Complexity Class)]]
- [[Parity Games are solvable in Qusaipolynomial time - introduction]]