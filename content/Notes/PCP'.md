---
tags:
  - Note
  - Incomplete
---
202502282202

Tags : [[Weighted Automata and Transducers]], [[Theory of Computation]]
# PCP'
---
>[!question]
>Given a bunch of dominoes, same as in [[Post Correspondence Problem|PCP]], let $P=\{ w_{1} \land w_{2} \}$, where $w_{1},w_{2}$ can be written as words together using the dominoes and $a \land b$ is the longest common prefix of $a$ and $b$.
>Is the set $P$ infininte.

This problem also happens to undecidable, because of a reduction from $PCP$.

The same example about a turing machine halting from the proof of [[Post Correspondence Problem|PCP]] works. Here any two consecutive transition will be differnt, so the largest work in $P$ could be as big as twice the size of the starting configurtion. And if there is a halting run, that configuration of dominoes can be repeated indefinitely to get an infinite set.

---
# References
