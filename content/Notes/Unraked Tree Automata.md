---
tags:
  - Note
  - Incomplete
---
202503141903

Tags : [[Automata Theory]], [[Finite Model Theory]]
# Unraked Tree Automata
---
>[!Definition]
>A (non-deterministic) tree automata is a tuple $\mathcal{A}=(Q, \Sigma,q_{0}, \delta)$ such that:
>- $Q$ is a finite set of states
>- $q_{0}$ is the start state
>- $\delta:Q \times \Sigma \to 2^{Q^*}$

Given a tree $T = (D, f)$, a run of $\mathcal{A}$ on $T$ is a function $r :D \to Q$ such that
- if $s$ is a node labelled $a$ with children $s \cdot 1, s \cdot 2 \dots s \cdot n$, then the string $r(s \cdot 1) r(s \cdot 2) \dots r(s \cdot n)\in \delta(r(s), a)$
- $r(\epsilon)=q_{0}$

The set of trees that have a run on the automata $\mathcal{A}$ is called the language of the automata.

---
# References
