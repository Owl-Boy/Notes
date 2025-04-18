---
tags:
  - Note
---
202504072004

Tags : [[Finite Model Theory]]
# Fagin's Theorem
---
**Fagin's Theorem** provides a purely logical characterization of the class [[NP (Complexity Class)|NP]].

>[!theorem] Theorem (Fagin)
>$\exists$[[Fragments of Second Order Logic#^f4d73e|SO]] [[Logic L capturing the complexity class K|captures]] [[NP (Complexity Class)|NP]].

Given an $\exists \text{SO}$ formula $\Phi$, one can first non-deterministically pick all the relations, and then use the polynomial algorithm for [[Complexity of FO#^586f2c|Data Complexity of FO]] to then solve it in polynomial time.

The proof for all $\text{NP}$ properties, there is a corresponding formula, we do a construction that is very similar to the proof of [[Trakhtenbrot's Theorem]]:

First we note that if a problem in in $\text{NP}$, then there is a polynomial $n^k$ such that for inputs of length $n$, a non-deterministic Turing Machine can solve it in time $n^k$.

The sentence describing a non-deterministic Turing machine $M$ that runs for at least $n^k$ steps can be described by the following sentence:

$$
\exists L, T_{0}, T_{1}, T_{2} H_{q_{0}}\dots H_{q_{m-1}} \Psi
$$
Where $L$ is a binary relation and all other relations have arity $2k$.

- We define $L$ to be linear order on the universe, with that defined, we can use it to make the lexicographical order on the $k$ tuples.
- $T_{0},T_{1},T_{2}$ represent the tape letters $0,1$ and empty.
- $H_{q}$ represents the head being in state $q$ in a particular position of the configuration.
- We also want
	- a configuration having exactly one head
	- transitions being consistent with the machine
	- there existing a final configuration
- The things that have to taken extra care of and which cannot be taken from the proof for [[Trakhtenbrot's Theorem]] are dealing with non-determinism and defining a start configuration.
	- For the non-determinism, one can take the disjunction of formulas defining transitions
	- To state the starting configuration, we create the formula $\iota(\vec{p})$ such that $\mathcal{A}\vDash \iota(\vec{p})$ iff the $p^\text{th}$ position of the encoding of the start state is $1$ and $\xi(\vec{p})$ which holds iff $\vec{p}$ comes after the definition of the start state, and hence we define 
	  $$
	  \forall \vec{p} \forall \vec{t}\left(\lnot \exists \vec{u}(\vec{u} <_{k} \vec{t}) \to \left[\begin{matrix}
        & \iota(\vec{p}) \leftrightarrow T_{1}(\vec{t}, \vec{p}) \\
        \land & \xi(\vec{p}) \leftrightarrow T_{2}(\vec{t}, \vec{p})
      \end{matrix}\right] \right)
	  $$
	- Now we need to define $\iota$ and $\xi$:
		- Since there are $n$ elements in the model that can be enumerated as $L$ defines a linear order, one can define addition and multiplication as relations in second order logic.
		- With that, if one wanted to talk about numbers up to $n^k$, one can consider a tuple of size $k$ which can be interpreted as a base $n$ number with $k$ digits.
		- Now for every single bit, one can explicitly write a formula with the above encoding of numbers and 
		  $$
		  \exists u, v \leq n-1 \left[ (n+1) + u \cdot n + v = \sum_{i=1}^k p_{i}n^{k-1} \land E(u,v) \right]
		  $$
		  For some binary relation $E$. This can be done for every single relation and then a disjuntion can be taken.

---
# References
