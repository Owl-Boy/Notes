---
id: The Category Graph is Monoidal
aliases:
  - The Category Graph is Monoidal
tags:
  - Note
---
202512272014

Tags : [[Discrete Homotopy Theory]]
# The Category Graph is Monoidal
---
>[!definition] 
> We define the box product $X \otimes Y$ of the two graphs as:
> $$
> \begin{align}
> (X \otimes Y)_V &= V_X \times V_Y\\
> (X \otimes Y)_E &= 
> \left \{
> (x, y)\sim(x', y')\middle|
> \begin{array}{l}
> x=x'\text{ and }y\sim y', \text{or} \\
> x\sim x'\text{ and }y=y'
> \end{array}
> \right\}\\
> &\cong (E_X \times V_Y)\sqcup (V_X \times E_Y)
> \end{align}
> $$

This definition differs from the [[Products and Coporducts|categorical product]] which defines edge set to be $E_X \times E_Y$.

It is fairly straight-forward to show that the product is associative and the graph $I_0$ works as the identity element of the product, this the category of graphs is a [[Monoidal Category]] under the $\otimes$ bifunctor with $I_0$ is the unit element.

Moreover with [[The Category Graph is Closed|The category Graph is Closed]]. We get that :

>[!theorem] 
> The category $\text{Graph}$ is a symmetric closed monoidal category.

---
# References
- [[Monoidal Category]]
- [[Products and Coporducts|products and Coporducts]]
- [[The Category Graph is Closed|The category Graph is Closed]].

