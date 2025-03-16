---
tags:
  - Note
  - Diagram
---
202404221904

Tags : [[Automata Theory]]
# Ranked Tree Automata
---
>[!tip] Why Trees
>Trees are a way to represent information in a fairly well structured way, a lot of times even strings semantically represent, like : 
>- `5 + 3 * 7`
>- `a \/ b /\ ~c`
>- Document formats like HTML and XML are also string representation of a tree structure
>
>These are likely to arise when the input has a structure more complicated than just a total order, hence a we study models that talk directly about trees.
>
>Notation and details about trees are discussed in [[Trees (Automata Theory)]]

>[!definition]
>A (non-deterministic) tree automaton is a tuple $A = (Q, q_{0}, \Sigma, \delta, F)$  such that:
>- $Q$ is a finite set of states
>- $q_{0}$ is the start state
>- $\Sigma$ is the labelling alphabet
>- $\delta:Q\times Q\times \Sigma \to 2^Q$ is the transition function.
>- $F \subseteq Q$ is a set of final states

>[!note] 
>The following description of runs is when trees are read from the leaves

Given a tree $t =(D, f)$, a run of $\mathcal{A}$ on $T$ is a function $r:D\to Q$ such that
- if $s$ is a leaf labelled $a$, then $r(s) \in \delta(q_{0}, q_{0}, a)$
- if $r(s \cdot 0)=q, r(s \cdot 1)=q'$ and $f(s)=a$, then $r(s)\in \delta(q, q',a)$

A run is called *successful* if $r(\epsilon)\in F$.

The set of trees that have a successful run on $\mathcal{A}$ is the language of the automata $\mathcal{A}$. 

---
# References
[[Trees (Automata Theory)]]
[[Ranked Trees in Logic]]