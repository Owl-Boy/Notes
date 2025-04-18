---
tags:
  - Note
---
202504101904

Tags : [[Finite Model Theory]]
# Fixed Point Logics
---

>[!tip] Motivation
>To talk about structures like graph, logics like [[First Order Logic|FO]] are not suitable because a lot of tractable properties of graphs, such as connectivity are not expressible in $\text{FO}$. Logics like [[Second Order Logic|SO]] and its variants like [[Monadic Second Order Logic|MSO]] are strong enough to even represent intractable properties. 
>
>The problem with the weaker logics is that a lot of graph properties like paths and connectivity can be stated with operators that can be constructed using fixed point operations and transitive closures. **Fixed Point Logics** extend $\text{FO}$ with operations that allow such computations.

To add a fixed point operator to $\text{FO}$, suppose we have a relational vocabulary $\sigma$ with an additional relation symbol $R$ with arity $r$. Let $\varphi(R, x_{1}\dots x_{r})$ be a formula with the above vocabulary.

For each $\mathfrak A \in \text{STRUCT}[\sigma]$, $\varphi(R, \vec{x})$ given an operator $F_{\varphi}:\mathcal P(A^k) \to\mathcal P(A^k)$ which is defined as:
$$
F_{\varphi}(X)= \{ \vec{a} \mid \mathfrak A\vDash \varphi(X/R, \vec{a}) \}
$$

Here $X / R$ means $R$ is interpreted as $X$.

## Logics

The logic $\text{IFP}$ is an extension of [[First Order Logic|FO]] with the following formulation rule:
- if $\varphi(R, \vec{x})$ is a formula, where $R$ has arity $r$ and $|\vec{x}|=|\vec{t}| = r$, for some $\vec{t}$, then
  $$[\text{ifp}_{R, \vec{x}}(R, \vec{x})](\vec{t})$$
  is a formula whose free variables are those of $\vec{t}$.
- The semantics are defined as
  $$
  \mathfrak A \vDash [\text{ifp}_{R, \vec{x}}(R,\vec{x})](\vec{a}) \text{ iff } \vec{a} \in \text{ifp}(F_{\varphi})
  $$

Similary, we can extend $\text{FO}$ to include partial fixed points to get the logic $PFP$.

To do the same for least fixed points, one needs to be careful as their existence is not guaranteed, unless $f$ is monotone, but it is [[Monotonicity is Undecidable|undecidable to check if a function is monotone]], so we can make a syntactic restriction that ensure monotonicity. Hence to define a logic with least fixed points, one must restrict to [[Positive Formulas]]. This logic is called $\text{LFP}$

>[!example]
>One can write $\text{LFP}$ formulae for
>- [[Acyclicity of Graphs is Definable in LFP|Acyclicity of Graphs]]
>- [[Arithmetic Operators are Definable in LFP|Arithmetic Operators]]

---
# References
