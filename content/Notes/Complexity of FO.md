---
tags:
  - Note
  - Incomplete
---
202502151502

Tags : [[Finite Model Theory]]
# Combined Complexity of FO
---
>[!theorem]
>The [[Combined Complexity of a Logic|Combined Complexity]] of [[First Order Logic|FO]] is [[PSPACE|PSPACE-Complete]].

The membership is $\text{P-SPACE}$ can be given by the following algorithm:
- Construct and Abstract Syntax Tree for $\Phi$. This will be checked recursively. So the argument will be inductive
	- If we are at a node with $\lnot$, by IH the child can be solved in $\text{P-SPACE}$ and this will require negligible space so we are done
	- If we are at a node with $\lor$, we solve 1 side, if false, we solve the other side, since both sides are $\text{P-SPACE}$ by IH, we are done
	- If we are at a node with $\exists x$, we replace the value of $x$ with $0$ initially, then we do it for the entire subformula from that point, and solve the lower part. Then we erase the working and replace $x$ with $1$ and we keep doing that. Since the subformula takes $\text{P{-SPACE}}$ and we keep reusing the space, we are done.
	- For the base case, to check atomic formulas in the vocabulary, we simply count the position of the vector we are checking and we see the encoding of the relation. This will be $\text{P-SPACE}$. So we are done.

To prove Hardness, we find a reduction form [[Quantified Boolean Formulas]]
- We Say the model is $A = \{ 0, 1 \}$ and there is one relation $\top = \{ 1 \}$.
- So the encoding of the model is $00101$ So the size of the input is $O(\|\Phi\|)$.
This reduced any QBF problem to a model checking problem with a $\text{P-TIME}$ reduction : adding $00101$ to the input and encoding the formula.

>[!lemma] Corollary
> [[Expression Complexity of a Logic|Expression Complexity]] of $\text{FO}$ is $\text{P-SPACE Complete}$ by the exact same proof.

>[!lemma] Corollary
>[[Data Complexity of a Logic|Data Complexity]] of $\text{FO}$ is [[P Complexity Class|PTIME]]. As if we use the above algorithm for membership in $\text{P-SPACE}$ for combined complexity. If $p$ is the size of the formula, then for each vertex in the AST of the formula, we have to do checks of size at most $\|A\|^p$, which will be at a $p$-depth quantifier chain. As checking atomic formula is polytime. So the time it takes is $O(\|\Phi\|\cdot\|\mathfrak A\|^{\|\Phi\|})$.



---
# References
