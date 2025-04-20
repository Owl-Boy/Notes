---
tags:
  - Note
---
202504191604

Tags : [[Weighted Automata and Transducers]]
# Rational Relations as Weighted Automata
---
We first describe the semi-ring we will be working in:
- If we want to describe an $n$-ary relation, then the set that we are working in is rational expressions for $n-1$-ary relations.
- The product operation would be concatenation
- The Sum operations would be union.

The automata can be constructed by looking at the multi tape automata, where we fix one of the tapes and allow the automata only run on the other tapes, and the rational relation we get from that is the output of the weighted automata on the word which was fixed in tape 1.

---
# References
