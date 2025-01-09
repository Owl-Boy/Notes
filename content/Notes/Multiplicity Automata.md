---
tags:
  - Note
  - Incomplete
---
202501092301

Tags : [[Automata Theory]]
# Multiplicity Automata
---
Multiplicity Automata are a variant of automata that work over different semantics. 

A regular [[Deterministic Finite State Automata]] can be thought of as a function from $\Sigma^* \to \{ \top, \bot \}$, or a classifier that is true if a word has an accepting run, and false otherwise. A multiplicity automata can be thought of as a function from $\Sigma^* \to \mathbb{N}$ which counts the number of accepting path each word has. 

The base model is the same, one words on a directed graph with edges labelled by alphabets with a dedicated start state and a subset of states as accept states.

>[!todo] TODO:Draw an example

---
# References
