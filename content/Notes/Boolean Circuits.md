---
tags:
  - Note
  - Incomplete
---
202502120102

Tags : [[Theory of Computation]], [[Complexity Theory]], [[Finite Model Theory]]
# Boolean Circuits
---
Boolean circuits are DAGs with a single sink node.

The sink node is supposed to hold the final value of the computation that is done by the circuit and the leaves represent inputs, while the other nodes represent boolean operations of $\land, \lor$ and $\lnot$.

>[!definition]
>A boolean circuits with $n$ inputs $x_{1}\dots x_{n}$ is a tuple
>$$
> C = \langle V, E, \lambda, o \rangle
>$$
>such that:
>- $(V, E)$ is a directed acyclic graph
>- $\lambda$ is a function from $V$ to variables or boolean operators
>	- $\lambda(v)=\lnot$ then the node as fan-in $1$
>- $o\in V$

This circuit computes a boolean function with $n$ inputs.

---
# References
