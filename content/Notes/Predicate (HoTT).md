---
tags:
  - Note
---
202507261407

Tags : [[Homotopy Type Theory]]
# Predicate
---
>[!definition]
>Given an **equivalence relation** on a type $A$, an equivalence class of the relation is called is a **predicate**. Thus, given a relation $R:A \times A \to\text{Prop}$ we can define $P:A\to\text{Prop}$ if there [[Mere Propositions|merely]] exists an $a:A$ such that for all $b:B$ we have $R(a, b)\simeq P(b)$. 

We define the set of Predicates over a relation as following:
$$
A /\!\!/ R :\equiv \{ P : A\to R \mid P \text{ is an equivalence class of }R\}.
$$
the function $q':A\to A /\!\!/R$ is defined by $q'(a):\equiv P_{a}$.

---
# References
- [[Mere Propositions]]
- [[Set Pushout]]