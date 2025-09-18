---
tags:
  - Note
---
202509131509

Tags : [[Games on Graphs]]
# Büchi-McNaughton Theorem
---
The following result was proven by Büchi in 1962 and McNaughton in 1966:
>[!theorem]
>For every formula in [[Monadic Second Order Logic]] of $\mathbb{N}$ with $\text{succ}$, one can construct an equivalent deterministic [[omega-Automata|Muller Automata]].

>[!example]
>Consider the specification
>$$
>\phi_{1}(X, Y) : \forall x. x\in X \Rightarrow x\in Y
>$$
>A Muller Automaton over $\{ 0,1 \}^2$ for $\phi_{1}$ is:
>![[Pasted image 20250913154109.png|400]]
>Where $\{ 1 \}$ is only set of good states. 


>[!example]
>Consider the specification
>$$
>\phi_{2} : \lnot \exists x. (x \not\in Y) \land \forall x', \text{succ}(x, x') \Rightarrow x' \not\in Y
>$$
>which states that there are no two consecutive zeros in the output.
>![[Pasted image 20250913155135.png|500]]
>where the accepting condition is $[\{ 1 \}, \{ 1, 2 \}]$.


---
# References
- [[Monadic Second Order Logic]]
- [[omega-Automata]]