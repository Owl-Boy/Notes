---
id: Graph
aliases: []
tags:
  - Note
---
202512271843

Tags : [[Discrete Homotopy Theory]]
# Graph
---
A graph $G = (V_G, E_G)$ is defined as a set of vertices $V$ along with a set of edges $E$ on $V$.

For the purposes of [[Discrete Homotopy Theory]], the edge relation is reflexive, that is, for any vertex $v \in V$ we have $(v, v) \in E$.

A *graph homomorphism* $f:G \to H$ is defined as a function on the underlying sets that respects the edge relation, that is:
$$
\forall (v_1,v_2 : V_G), (v_1, v_2)\in E_G \Rightarrow (f\ v_1, f\ v_2) \in E_H
$$

Thus, for the purposes of [[Discrete Homotopy Theory]], a map $f:G\to H$ is defined by a function that takes adjacent vertices $x,x' : G$ and either sends both of then to the same vertex, or sends then to adjacent vertices. 

---
# References

