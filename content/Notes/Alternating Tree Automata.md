---
tags:
  - Note
aliases:
  - Tree Automata
---
202511162211

Tags : [[Games on Graphs]], [[Automata Theory]]
# Alternating Tree Automata 
---
>[!note]
>The definition of trees used for all constructions and proofs is given [[Definition of a Tree as a language over words|here]], but it will be easier to consider them as a god-given mathematical structure. Note that each edge the child of a root has a unique number (direction associated with it), we say given a vertex $v$ the next vertex in direction $d$ is given by $w=d(v)$

## Definition
This is the most general form we will be looking at here.

>[!definition]
>This is given as a 7-tuple $\cal A$ containing the following information:
>- $\Sigma$, which is a finite set of labels
>- $D$, which is a finite prefix of $\mathbb{N}$, being the set of directions
>- $Q$, set of states of the automata
>- $q_\text{in}$, initial state
>- $\delta:Q\times \Sigma \to\mathcal B^+(D\times Q)$, which is the set of transitions that takes a state and a letter, and returns a positive boolean combination of elements from $D\times Q$.
>- $\alpha \subseteq Q^\omega$, which is an accepting condition on runs.

The size of the automaton $|\mathcal A|$ is the sum of sizes of all formulae.
## Runs of an Alternating Tree Automaton on a tree
Consider an automaton $\cal A$ and a $\Sigma$-labelled $D$-trees like $\mathcal T =(T, \tau)$. 

>[!tip] Intuition
>A run of an automaton on a word can be through of as taking the string, and folding it along the edges and vertices of the automaton, we will do something similar for trees. Since the automaton is alternating, we would have to take care of universal runs too, which we will include as a part of our run. This will be given as a tree labelled with $T\times Q$, which is like imagining a tree being wrapped around the automata and the nodes getting marked with the states.

A run of the automaton $\cal A$ on the trees can be defined as a $(T\times Q)$-labelled $\mathbb{N}$-tree $\Lambda= (\Gamma,\gamma)$ such that:
- $\gamma(\text{root}_{\Gamma})=(\text{root}_{T},q_{\text{in}})$
	- we start by reading the root from the start state
- If we are reading a vertex $(v,a)$ of the tree $\mathcal T$ from state $q$, then
	- we are at a vertex $w$ in $\Lambda$ labelled as $(v, q)$
	- Let $\{ (d_{1}, q_{1}), (d_{2},q_{2})\dots (d_{m},q_{m})\}$ be a set that satisfies the formula $\delta(q, a)$.
	- We add $m$ children to $w$ with labels $(d_{1}(v), q_{1}), (d_{2}(v),q_{2})\dots$

A run $(\Gamma, \gamma)$ is accepting if all infinite paths satisfy the condition $\alpha$, and a tree is accepted, if if it has an accepting run.

## Special Cases
- An automaton is called **non-deterministic** if, when the formulas of transitions are written in disjunctive normal form, each conjunctive term has at most 1 element for each direction.
- An automaton is called **universal** if the formulas in its transitions can be written only using conjunctions.
- An automaton is called **deterministic** if it is both universal and non-deterministic.
- If $|D|=1$ then we can called these **word-automata**.

---
# References
- [[Definition of a Tree as a language over words]]
- [[Alternating Turing Machine]]
- [[Alternating Finite Automaton]]