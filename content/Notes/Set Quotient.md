---
tags:
  - Note
---
202507252307

Tags : [[Homotopy Type Theory]]
# Set Quotient
---
An important [[Limits and Colimits|colimit]] of sets is the _quotient_ by a relation. Let $A$ be a set and let $R:A \times A \to\text{Prop}$ a family of [[Mere Propositions]] (a **mere relation**). Its quotient should be the [[Equalizers and Coequalizers|set-coequalizer]] of the 2 projections:
$$
\sum_{a,b:A}R(a, b)\rightrightarrows A
$$
And this can also be directly described by the following [[Higher Inductive Types|higher inductive type]].
- A function $q:A \to A /R$
- For each $a, b:A$ such that $R(a, b)$, an equality $q(a)=q(b)$
- A [[Truncation|set truncation]] constructor: for all $x, y:A/R$ and $r,s:x=y$ we have $r=s$.
---
# References
- [[Equalizers and Coequalizers]]
- [[Mere Propositions]]
- [[Truncation]]
- [[Limits and Colimits]]
- [[Higher Inductive Types]]