---
tags:
  - Note
---
202503141903

Tags : [[Finite Model Theory]], [[Automata Theory]]
# Regular Tree Languages are MSO definable
---
A **Tree Language** is called *Regular* if it is accepted by a [[Ranked Tree Automata]] or an [[Unraked Tree Automata]].

>[!Theorem]
>A set of [[Ranked Trees in Logic|trees]] is definable in [[Monadic Second Order Logic|MSO]] iff it is *regular*.

Given an automaton $\mathcal{A}$, to find an $\text{MSO}$ formula that accepts it, for each state $q$ we guess the set $X_{q}$ where the run of $\mathcal{A}$ is in state $q$, and then check in [[First Order Logic|FO]] for each leaf labelled $a$ is in $X_{q}$ for some $q\in \delta(q_{0}, q_{0}, a)$, that the transitions are consistent and the root is in some accepting states. This creates an $\exists \text{MSO}$ sentence.

The proof in the other direction is again very similar to that of the string case: [[MSO on Finite Words accept Regular Languages]]
- Let $\Phi$ be the formula with [[Notes/Quantifier Rank|Quantifier Rank]] $k$. Let $\tau_{0}\dots \tau_{m}$ be the [[Rank-k m,l Types MSO|MSO types]] and $t_{0}$ be the type of the empty tree.
- We let $\tau_{0}\dots \tau_{m}$ be the states of the automata
- We let $\tau_{0}$ to be the start states
- Given a tree $t=(t_{1}, \text{node}, t_{2})$ with label $a$ we have $[\![t]\!]\in \delta([\![t_{1}]\!], [\![t_{2}]\!], a)$
- We let the set of final states be the set of types consistent with $\Phi$.

>[!theorem] Corollary
>For every formula $\Phi$ in $\text{MSO}$ over trees, there is an equivalent $\exists\text{MSO}$ formula $\Phi'$

The proof is identical for [[Unranked Trees in Logic]]

---
# References
[[MSO on Finite Words accept Regular Languages]]