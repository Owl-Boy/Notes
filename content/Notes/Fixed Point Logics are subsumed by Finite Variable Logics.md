---
tags:
  - Note
  - Incomplete
---
202504291904

Tags : [[Finite Model Theory]]
# Fixed Point Logics are subsumed by Finite Variable Logics
---
>[!theorem]
>$\text{LFP}$ is subsumed by $\mathcal{L}_{\infty, \omega}^\omega$.

To show this, we do something similar to what we do in [[Paths on Graphs and Finite Variable Logics]]. 

Given a formula $\Psi(K, \vec{x})$ we construct the fixed point as follows:
- $\Psi_{0} = \bot$
- $\Psi_{n+1} = \Psi(\Psi_{n}/K, \vec{x})$

That is in the following definition:
$$
\Psi_{n+1}(\vec{x}) = \big[\dots R(\vec{z}) \dots\big]
$$
where we want to replace $R(\vec{z})$ with $\Psi_n(\vec{z})$, and we do that as follows in fixed variable logics. We replace $R(\vec{z})$ with:
$$
\exists \vec{x}(\vec{x} = \vec{z} \land \Psi_{n}(\vec{x}))
$$.

This is because in the definition of $\Psi_{n}$, $\vec{x}$ of the outer scope is no longer required, hence we reuse it.

Thus for a formula with $n$ variables in $\text{LFP}$, one can write an equivalent formula in $\mathcal{L}_{\infty, \omega}^\omega$ with $2n$ variables.

---
# References
