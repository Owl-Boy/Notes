---
tags:
  - Note
  - Incomplete
---
202505080005

Tags : [[Homotopy Type Theory]]
# Peano Axioms and Type Theory
---
The following are the Axioms for natural numbers as given by Peano:
- There is a natural numbers $0$
- For every natural number, there is a successor
- One can induct on natural numbers
- The successor function is injective
- There is no natural number whose successor is $0$

Now consider the definition of [[Natural Numbers in Type Theory]].
- We have the constructor $0$
- We have the constructor $\text{succ}$
- The elimination rule is essential the axiom on induction.

The 2 peano axioms that are left out can be proven as theorem from what we proved in [[Higher Groupoid Structure of Natural Numbers]]!!
- There is no natural number which is a successor of $0$
  Here we have $\prod_{m:\mathbb{N}}\text{encode}(\text{succ}(m),0) \to \mathbf{0}$.
- To show that the successor function is injective we have
  $$
\begin{align}
(\text{succ}(m)= \text{succ}(n)) \xrightarrow{\text{encode}}\ &\text{code}(\text{succ}(m), \text{succ}(n)) \\
\equiv\ &\text{code}(m, n) \\
{}\xrightarrow{\text{decode}}\ &(m=n) 
\end{align}
  $$

---
# References
