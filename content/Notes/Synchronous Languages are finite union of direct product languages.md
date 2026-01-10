---
id: Synchronized Languages are union of Direct Product Languages
aliases:
  - Synchronized Languages are union of Direct Product Languages
tags:
  - Note
---
202601102205

Tags : [[Concurrency Theory]]
# Synchronized Languages are union of Direct Product Languages
---
> [!thm] Theorem 
> Every language that is recognized by a [[Syncho]] iff it can be written as a finite union of [[Distributed Product Automata|Direct Product Languages]].

## Forward 
If a language is recognized by a Synchronzied automata $A$ with set of final states $F$, then for each final state $f\in F$, construct a synchronized automata $A_f$ with a singleton set final state $\{f\}$. Each $A_f$ is also a direct product automata. The language accepted by $A$ is the union of languages accepted  by any $A_f$.

## Backward
Given a finite union of direct product languages, each for each language we can create a direct product automata $A_i$, For each process $p$ and for each automata $A_i$ we can find a process automata $A_i^p$which accepts the language of $A_i$ projected to $p$.

Fixing a $p$ we can take the product of each $A_p^i$, and for each $i$ we can $A_p^i$ with a copy of the product such that it accepts the same language.

Now all direct product automata have the same underlying transition system, and hence we construct a synchronized automata by taking same transition system with the final states being the union of all final states.

---
# References
- [[Direct Product Automata]] 
- [[Concurrency Theory]]
- [[Direct Product Automata are not closed under boolean operations]]
