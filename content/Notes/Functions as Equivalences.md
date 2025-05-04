---
tags:
  - Note
  - Incomplete
---
202505041305

Tags : [[Homotopy Type Theory]]
# Functions as Equivalences
---
>[!definition]
>Given a function $f:A \to B$ we call it a *quasi-inverse* if it satisfies the following property:
>$$
>\text{qinv}(f) :\equiv\sum_{g:B\to A} \big((f \circ g \sim \text{id}_{B}) \times (g \circ f \sim \text{id}_{A})\big)
>$$

might seem odd to call this as the definition of quasi-inverse, even though it very cleanly captures what we want, we want the existence of a function $g$, the composition of these functions is homotopic to identity. But this type is not well behaved, it may have multiple unequal elements in it.

>[!Definition] 
>Given a function $f:A \to B$, we can it an equivalence if the following type is inhabited:
>$$
>\text{isequiv}(f) :\equiv \left( \sum_{g:B \to A} (f \circ g \sim \text{id}_{B}) \right) \times \left( \sum_{h:B \to A} (h\circ f \sim \text{id}_{A}) \right) 
>$$

This definition satisfies the following properties:
- For each $f:A \to B$, the definitions are logically equivalent in the sense
	- There is a function of type $\text{qinv}(f) \to \text{isequiv}(f)$
	- There is a function of type $\text{isequiv}(f) \to \text{qinv}(f)$
- For any 2 inhabitants $e_{1}, e_{2}:\text{isequiv}(f)$ we have $e_{1}=e_{2}$.

For the first point we have the following proofs:
- $\text{qinv}(f) \to \text{isequiv}(f):\equiv (g,\alpha, \beta) \mapsto ((g, \alpha),(g, \beta))$
For the other direction note the following:
$$
g \overset{\beta}{\sim} h\circ f \circ g \overset{\alpha}{\sim}g
$$
And we can write the composite as $\gamma(x) = \beta(g(x))^{-1}\cdot h(\alpha(x))$. Now we can define $\beta': g\cdot f \sim \text{id}_{A}$ as $\beta(x) :\equiv \gamma(f(x)) \cdot \beta(x)$, then we can define the function:
$$
\text{isequiv}(f) \to \text{qinv}(f) :\equiv ((g, \alpha), (h, \beta)) \mapsto (g, \alpha, \beta')
$$

The third point we will post pone.

Now given 2 types we can finally define an equivalence between them:
>[!definition]
>Given 2 types $A$ and $B$ we define an equivalence between them as follows:
>$$
>A \simeq B :\equiv \sum_{f:A\to B} \text{isequiv}(f)
>$$

It is also clearly an equivalence relation.


---
# References
