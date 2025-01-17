---
tags:
  - Note
---
202501162301

Tags : [[Weighted Automata and Transducers]]
# Threshold Languages
---
For a weighted automata over a semi ring that is ordered, a threshold language is the set of words whose weight satisfy some constraints generally written as:
$$
L_{\bowtie s} = \{ w | f(w) \bowtie s \}
$$
where $\bowtie$ is any of $\{  <, \leq, =, \geq, > , \neq \}$ and $s\in \mathbb{Z}$.

>[!example]
>- $L_{\neq 0}$ : This is the set of words that have a non-zero weight, also called the *support* of an automata.
>- $L_{>0}$ : This is the set of words with positive weights.

>[!note]
>These languages are non necessarily regular, for example:
>- Consider the following function $f = \#a - \#b$. The support for this language is the set of words where the number of $a$s is not equal to the number of $b$s, which is not regular.
>
>The support is regular over monoids that are zero-sum free.

---
# References
