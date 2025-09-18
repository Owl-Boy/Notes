---
tags:
  - Note
  - Incomplete
---
202509131509

Tags : [[Games on Graphs]]
# Muller Automata to Games
---
Consider the examples in [[Büchi-McNaughton Theorem]]. 

The examples construct an automata given a specification in S1S. This automata, accepts those words which correspond to a valid output stream given the corresponding input, but this does not directly given a way to generate output, for examples.


![[Pasted image 20250913155135.png|500]]

Which accepts cases where there are no two consecutive 0s in the output, After returning some amount of bits, say that we are in state 1. Then it is unclear whether we should remain in this state or move to state two (does not matter much for this example, but it does not more sophisticated ones).

Thus there is a need to resolve this non-determinism, and a solution to that is called a "strategy".

To formalise the above idea, we define [[Games on Graphs#^68e6da|Games]].

---
# References
