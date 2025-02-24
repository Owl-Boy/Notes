---
tags:
  - Note
  - Incomplete
---
202501092301

Tags : [[Automata Theory]], [[Weighted Automata and Transducers]]
# Weighted Automata
---
A *weighted automata* is a generalization of the [[Multiplicity Automata]] that allows one to replace parallel weights with edge weights. The intuition is direct, 2 parallel edges will be replaced with an edge of weight $2$. 

But weighted automata allow one to put negative inputs as well, and the semantics of the automata become as follow.
- The weight of a word is the sum of weights of all accepting paths of the word.
- The weight of an accepting path is the product off weights of all edges of the paths.

With this change in semantics, one does not necessarily need to work with natural numbers of integers. It can be defined over any [[Semi Ring]].

>[!todo] TODO: Draw an  example

>[!theorem] 
>A weighted automata over the boolean semi ring: $\langle \{ \top, \bot \}, \lor, \land, \top, \bot \rangle$ is just a regular automata.

>[!Definition]
>A weighted automata is the following 4-tuple
>$$
>\langle Q, \{ \mu_{a} \}_{a\in \Sigma}, I, F \rangle
>$$
>where
>- $Q$ is the set of states.
>- For each letter $a$ in the alphabet, we have a transition from any state $q_{1}$ to $q_{2}$ this is given by $\mu_{a}: Q \times Q \to S$.
>- $I:Q \to S$ is the weights assigned to the start states.
>- $F: Q \to S$ is the weights assigned to final states.

>[!attention] Notation
>If in a diagram, an edge is drawn without a weight associated with it, we assume it to be $1$. If an edge is not drawn, we assume its weight to be $0$.

>[!definition] Run
>The *run* of a word $w=a_{1}a_{2}\dots a_{n}$ is the sequence of states $s=q_{0},q_{1}\dots q_{n}$, and the weight of a run is defined as
>$$
>\text{wt}(s) = I(q_{0}) \cdot \mu_{a_{1}}(q_{0}, q_{1})\dots \mu_{a_{n}}(q_{n-1}, q_{n}) \cdot F(q_{n})
>$$
>weight of a word is the sum of weights of all the runs of a word.


---
# References
[[Multiplicity Automata]]
[[Semi Ring]]