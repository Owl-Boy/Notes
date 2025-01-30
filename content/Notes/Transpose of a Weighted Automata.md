---
tags:
  - Note
---
202501201601

Tags : [[Weighted Automata and Transducers]]
# Transpose of a Weighted Automata
---
>[!note] This is the WA version of reversing a language

A Weighted automata is a function $f: \Sigma^* \to S$, where $S$ is a semi-field. A good interpretation for the reverse of a weighted automata would be the following function $g : f \circ\text{rev}$. An attempt at this could be the following:
- $I' = F^T$
- $\mu_{a}' = \mu_{a}^T$
- $F' = I^{T}$

The above operation is called the *Transpose* of a weighted Automata.

Unfortunately, since produce of elements in a weighted automata is not necessarily commutative, we do not have that $f(w)=f(\text{rev } w)$ for a given run.

---
# References
