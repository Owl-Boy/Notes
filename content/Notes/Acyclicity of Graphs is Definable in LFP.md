---
tags:
  - Note
  - Incomplete
---
202504111804

Tags : [[Finite Model Theory]]
# Acyclicity of Graphs is Definable in LFP
---
The property of a *directed graph* being **acyclic** can be described using a fixed point of a procedure as follows:
- Start by marking the sources in the graph, if the graph is non-empty and acyclic then it must contain sources.
- We then mark all vertices whose parents are only marked vertices. 
- If the graph does not contain a cycle, then it will eventually cover the entire graph.

A proof for the algorithm is as follows:
- If the graph has a cycle, and the cycle is not marked, then in the step, no vertex in the cycle can be marked, hence the cycle will remain unmarked
- If the graph is a cyclic, then one can do a toposort on it and on each step at least the vertex with minimum value will be marked.

One this needs to define an operator that behaves as descrived:
$$\varphi(S, x) :\equiv \forall y\big[E(y, x) \to S(y)\big]$$

With that described, the following is an [[Fixed Point Logics|LFP]] logic for acyclicity of graphs:
$$
\Phi :\equiv \forall u,\; [\text{lfp}_{S,x}\varphi(S, x)](u)
$$

---
# References
