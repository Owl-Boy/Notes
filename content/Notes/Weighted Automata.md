---
tags:
  - Note
  - Incomplete
---
202501092301

Tags : [[Automata Theory]]
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

---
# References
[[Multiplicity Automata]]
[[Semi Ring]]