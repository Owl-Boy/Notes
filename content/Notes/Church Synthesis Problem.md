---
tags:
  - Note
---
202508122108

Tags : [[Games on Graphs]], [[Logic]]
# Church Synthesis Problem
---
Alonzo Church posted the *Synthesis* problem in 1957. The problem statement was as follows:
>[!question]
>The model used for this problem is a device ([[Büchi Automata]]) that accepts an input stream of bits and each time it receives a bit, it returns a bit. Given a specification for requires output based on the input. The problem asks if its possible to build such a device that satisfies the specification by construction.

The input of the synthesis problem is a specification given in [[Monadic Second Order Logic]] for [[Strings in Logic|strings]].

The following are possible outputs are:
- A [[omega-Automata#^eda855|Muller Automata]] that satisfies the specification
- 'No', stating that no such automata exists.

---
# References
- [[Büchi Automata|Buchi Automata]]
- [[omega-Automata]]
- [[Monadic Second Order Logic]]
- [[Strings in Logic]]