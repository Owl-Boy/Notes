---
tags:
  - Note
  - Incomplete
---
202505172305

Tags : [[Homotopy Type Theory]]
# Type Formers and Mere Propositions
---
The goal for describing [[Mere Propositions]], was to have a subset of types where logic behaves in a more usual way of things being assigned true of false.

This will only be possible if the type formers preserve the property of mere propositions:

>[!lemma]
>If $A$ and $B$ are mere propositions, then $A \times B$ will be a mere proposition. This behaves like logical conjunction.

>[!lemma]
>If $A$ is any type and $B:A \to\mathcal U$ is a type family such that $B(x)$ is a mere proposition for all $x:A$ then $\prod_{x:A}B(x)$ is a mere proposition. This behaves like logical implication.

What we are missing is disjunctions and unfortunately $\mathbf{2}$ is not a mere proposition even though $\mathbf{1}$ is. That is because coproducts do not just store the fact that one of the 2 types is inhabitied, they also store which one.

In order to preserve mere proposition we would want to "[[Propositional Truncation|truncate]]" a type by forgetting additional information.

The same issue arises with $\Sigma$ types.

---
# References
[[Propositional Truncation]]
