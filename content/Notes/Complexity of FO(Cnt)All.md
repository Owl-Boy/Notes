---
tags:
  - Note
  - Incomplete
---
202504290104

Tags : [[Finite Model Theory]]
# Complexity of $\text{FO(Cnt)}_{\text{All}}$
---
Consider the extension of $\text{FO(Cnt)}$ to $\text{FO(Cnt)}_{\text{All}}$, this logic has a linear ordering on the first sort and has a restriction of every predicate on natural numbers to the first sort.

>[!theorem]
>The class of all structures definable by an $\text{FO(Cnt)}_{\text{All}}$ sentences is in non-uniform $\text{TC}_{0}$. This the data-complexity of $\text{FO(Cnt)}_{\text{All}}$ is non-uniform $\text{TC}_{0}$.

Since we have all predicates on natural numbers, we can assume the base universe to also work as the universe of the second sort, that is, we can write the following:
$$
\exists yx \varphi(x, \dots)
$$
where we interpret $y$ as $i$ where $y$ is the $i^\text{th}$ element of the universe.


We will now build a series of circuits for different sizes of models:
- If the formula is of form $S(\vec{x})$ which is an atomic formula, then one can simply replace it with the corresponding bit in the encoding.
- For Boolean connectives, we simply use boolean nodes of the circuits
- For standard quantifiers, one can simply treat them as finite conjunctions or disjunctions as we know the size of the model
- For counting quantifiers of the form $\exists x_{1}y\ \varphi$, one needs to show that there are at least $x_{1}$ many $y$s that satisfy it, for that, one can use a $\text{Maj}$ node, where it takes $2n$ inputs, where the first $n$ inputs would be answer for all possible $y$'s and the next $n$ inputs would have $n-x_{1}$ $1$s and the rest $0$, hence there will be a majority of $1s$ iff the condition satisfies.

This construction is clearly constant depth, it only depends on the formula, and polynomial in the size of the input.


---
# References
