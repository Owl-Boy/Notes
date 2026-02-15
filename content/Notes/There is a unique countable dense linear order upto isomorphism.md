---
id: There is a unique countable dense linear order upto isomorphism.Model Theory
aliases:
  - There is a unique countable dense linear order upto isomorphism.Model Theory
tags:
  - Note
---
202602151632

Tags : [[Model Theory]] [[Order Theory]]
# There is a unique countable dense linear order upto isomorphism.Model Theory
---
> [!THM]
> The Theory DLO is $\aleph_0$-categorical and complete.

Let $(A, <)$ and $(B, <)$ be two countable models of DLO. Let $a_0,a_1\dots$ be an enumeration of $(A,<)$ and let $b_1,b_2\dots$ be an enumeration for $(B, <)$

We will build a bijection by building a sequence of partial bijection, considering one extra element form each partial order at a time.

We define $A_i = \{a_1\dots a_n\}$ and $B_i = \{b_1\dots b_n\}$.

We define $f_0 : A_0 \to B_0$, there is a unique function that satisfies this.

At stage $n+1$, let $a_{n+1}$ be the first element in $A$ (according to the enumeration) that is not in $A_n$. This will lie in between 2 elements $a_i$ and $a_j$, thus for the element $b_{n+1}$, we pick an element that is in between $b_i$ and $b_j$. Similar arguments holds if $a_{n+1}$ is bigger or smaller than $A_n$. We then do the same procedure with roles of $A$ and $B$ reversed.

Since DLO has no finite models by [[Vaught Test]], we can say that it is complete.

---
# References
- [[Ehrenfeucht-Fraïssé Game]]
- [[Vaught Test]]

