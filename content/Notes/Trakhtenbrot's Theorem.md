---
tags:
  - Note
  - Incomplete
---
202504060604

Tags : [[Finite Model Theory]]
# Trakhtenbrot's Theorem
---
>[!theorem]
>For every relational vocabulary $\sigma$ with at least 2 binary relation symbol, it is undecidable whether a sentence $\Phi$ of a vocabulary $\sigma$ is finitely satisfiable.

The proof proceeds by constructing a formula $\Phi_{M}$ for every [[Turing Machines|turing machine]] $M$ such that the models that satisfy $\Phi_{M}$ correspond to [[Computational History]] of $M$.

>[!attention] Notation
>Here we are assuming there is 1 accept state and 1 reject state. We assume our tape alphabet to be $\{ 0, 1 \}$ also, since we are starting with empty string, we assume $0$ behaves as the blank alphabet.

If the turing machine is defined as follows:
$$
M = \langle Q, \Sigma, \Delta, \delta, q_{0}, q_{a},q_{r}\rangle
$$
we build the corresponding formula with the following vocabulary:
$$
\sigma = \{ <, \text{min}, T_{0}(-,-), T_{1}(-,-), (H_{q}(-,-))_{q\in Q} \}
$$

>[!note] multiple binary relations
>The theorem promised $1$ binary relation, here we are assuming multiple. This is fine as we can encode multiple relations into 1 relation.
>
>This can be done in the following way:
>- We create a directed graph such that some vertices represent nodes in the multiple relations situation, while other vertices represent edges:
>- Nodes such that $R(x, x)$ holds will be vertices.
>- Nodes where that property does not hold will be in cycles of length upto $n$ and can connects to exactly 2 vertex nodes. 

Explicit construction of the formula is give in [[Trakhtenbrot's Encoding of Turing Machine]], but the idea is given below:
- We have 1 formula that states $<$ is an ordering relation
- We define $\text{min}$ to be the smallest element in the model
- For all the other relations, we treat the first argument as the configuration step of the machine and the second argument as the position in the configuration
	- We first have a formula to state that the first configuration is the start configuration
	- Then we have a formula to state that there is some final configuration
	- A formula encoding transitions
- And we also have the following formulas ensuring the following:
	- each node is labelled either 0 or 1 and not both
	- each configuration has exactly 1 position labelled with a vertex

---
# References
