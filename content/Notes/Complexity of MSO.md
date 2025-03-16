---
tags:
  - Note
  - Incomplete
---
202503160103

Tags : [[Finite Model Theory]], [[Complexity Theory]]
# Complexity of MSO
---
>[!theorem]
>The [[Combined Complexity of a Logic|Combined Complexity]] of [[Monadic Second Order Logic|MSO]] is [[PSPACE|PSPACE-Complete]]

The problem being $\text{PSPACE-Hard}$ directly comes from the [[Complexity of FO]].

For a $\text{PSPACE}$ algorithm, Consider a model encoded in the way described in [[Encoding Finite Model]] and a formula that can be given as a string:
- One first creates an abstract syntax tree for the formula and that will be used to inductively show that the argument holds in a way that is very similar to [[Complexity of FO]]
	- If we are at a node with $\lnot$, by IH the child can be solved in $\text{P-SPACE}$ and this will require negligible space so we are done
	- If we are at a node with $\lor$, we solve 1 side, if false, we solve the other side, since both sides are $\text{P-SPACE}$ by IH, we are done
	- If we are at a node with $\exists x$, we replace the value of $x$ with $0$ initially, then we do it for the entire subformula from that point, and solve the lower part. Then we erase the working and replace $x$ with $1$ and we keep doing that. Since the subformula takes $\text{P{-SPACE}}$ and we keep reusing the space, we are done.
	- We represent quantification over a relation the same way any other relation is represented, just the algorithm is looped repeatedly with different relations for every quantifications until the formula is satisfied or the algorithm checks every single relation.
	- For the base case, to check atomic formulas in the vocabulary, we simply count the position of the vector we are checking and we see the encoding of the relation. This will be $\text{P-SPACE}$. So we are done.

>[!theorem] Corollary
>[[Expression Complexity of a Logic|Expression Complexity]] of [[Monadic Second Order Logic|MSO]] is $\text{PSPACE-Complete}$ by the same proof.

---
# References
