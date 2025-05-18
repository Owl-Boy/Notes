---
tags:
  - Note
  - Incomplete
---
202505182305

Tags : [[Homotopy Type Theory]]
# A better Axiom of Choice for Type Theory
---
Assume a type $X$ and type families:
$$
A : X\to \mathcal U\quad \quad\text{and}\quad \quad P:\prod_{x:X}A(x) \to \cal U
$$
and that
- $X$ is a set
- $A(x)$ is a set for every $x:X$
- $P(x, a)$ is a [[Mere Propositions|mere proposition]] for all $x:X$ and $a:A(x)$.

>[!axoim]
>Then the **Axiom of Choice** $\text{AC}$ states:
>$$
>\Big(  \prod_{x:X}  \Big\|\sum_{a:A(x)} P(x,a) \Big\|\Big) \to \Big\| \sum_{g:\prod_{(x:X)}A(x)}  \prod_{x:X} P(x, g(x)) \Big\|
>$$

This can be written in the more standard notation of 
$$
\Big( \forall (x:X). \forall(a:A(x)).P(x, a)\Big) \Rightarrow \Big(\exists (g: \Pi_{(x:X)}A(x)).\forall (x:X).P(x, g(x))\Big)
$$
But note that we also know that the above is an equivalence

>[!lemma]
>The axiom of choice is equivalent to the following statement:
>For any set $X$ and any $Y: X \to \cal U$ such that $Y(x)$ is a set for all $x:X$ then 
>$$
>\Big( \prod_{x:X} \| Y(x) \| \Big) \to 
>\Big\|\prod_{x:X} Y(x) \Big\|
>$$
>Which reads as: *The cartesian product of a family of non-empty sets is non-empty*

To prove that statement, we have that the codomain is equivalent to 
$$
\Big\| \prod_{x:X} \sum_{a:A(x)} P(a, x)\Big\|
$$
where $Y(x)=\sum_{a:A(x)}P(a, x)$. Conversely, we can let $A(x) = Y(x)$ and let $P(x, a):\equiv 1$, hence both of these are logically equivalent, but both of them are mere propositions, so they are equal types.

Also note that since both sides of $\to$ are mere propositions, and the right implies the left, which is easy to show, we simply take propositional truncation in side the codomain, and we can then remove the outer one.



---
# References
