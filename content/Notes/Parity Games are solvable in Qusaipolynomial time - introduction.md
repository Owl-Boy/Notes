---
tags:
  - Note
  - Incomplete
  - MOC
---
202509301409

Tags : [[Games on Graphs]]
# Parity Games are solvable in Qusaipolynomial Time - MOC
---
This will be a rewrite of chapter 9 of [The Automata Toolbox](https://www.mimuw.edu.pl/~bojan/paper/automata-toolbox-book) by Mikołaj Bojańczyk dealing with the following theorem:

>[!theorem]
>Parity games with $n$ positions and $d$ ranks can be solved in time $n^{O(\text{log }d)}$.

Whether or not it is possible to solve parity games in polynomial time of $n$ and $d$ is an open problem, the proof of this result will this be an algorithm that solves a parity games in [[Quasi-Polynomial time]].

The rough sketch of the proof will be starting with looking at a simpler game, called the [[omega-Automata|Reachability Automata]]. Then we create an automata by taking the product of this Reachability game with the parity game in question, the language of this automata will correspond to strategies that can be used in the parity game ([[Reachability Automata for Parity Games]]).

Thus the core part of the proof will be constructing a succinct reachability automata with good time complexity. ([[Exponential Reachability Automata for Parity Games]] then [[Succinct Reachability Automata for Parity Games]])

## Notes
- [[Quasi-Polynomial time]]
- [[omega-Automata|Reachability Automata]]
- [[Reachability Automata for Parity Games]]
	- [[Exponential Reachability Automata for Parity Games]]
	- [[Succinct Reachability Automata for Parity Games]]

---
# References
[[Reachability Games and Friends]]