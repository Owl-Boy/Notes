---
tags:
  - Note
  - Incomplete
---
202503310203

Tags : [[Homotopy Type Theory]]
# Path Induction
---
Before we get to the **Induction Principle** Lets look at the recursion principle called *Indiscernibility of identical*:
>[!note] Recursion Principle : Indiscernibility of Identicals
>For every family 
>$$C:A\to\cal U$$
>there is a function
>$$
>f:\prod_{x, y:A} \prod_{p: x=_{A}y} C(x) \to C(y)
>$$
>such that
>$$
>f(x, x, \text{refl}_{x}) :\equiv \text{id}_{C(x)}
>$$

^4e1620

Indiscernibility of Identicals states that if there are 2 equal elements $x, y:A$ then any family from $A \to \cal U$ must have equal elements going to "equivalent types" as witnessed by the function. This is one of the ways equality if respected 

The notion of equivalent types will be discussed later.

The induction principle for equality types is called *path induction*

>[!note] Path Induction
>Given a family
>$$C:\prod_{x,y:A}(x=_{A}y) \to \cal U$$
>and a function
>$$c: \prod_{x:A} C(x, x, \text{refl}_{A})$$
>there is a function
>$$
>f: \prod_{(x, y:A)} \prod_{(p: x=_{A}y)} C(x, y, p)
>$$
>such that 
>$$f(x, x, \text{refl}_{x}) :\equiv c(x)$$

To understand the above statement, consider the constant case, here if you have a predicate $C(a, b)$ such that $C(x, x)$ is always true, if we have a $y$ such that $x=y$ we should have that $C(x, y)$ to be true, in general, the above holds with the addition that it respects the fact that there are multiple witnesses for equality.

Equality also respects paths in the homotopy interpretation.

All of this can be packaged up into the induction function:
$$
\text{ind}_{=_{A}} : \prod_{\left( C:\prod_{(x, y:A)}(x=_{A}y) \to \mathcal U \right)} \left( \prod_{(x:A)} C(x, x, \text{refl}_{x}) \right) \to \prod_{(x, y:A)} \prod_{p: x=_{A}y}C(x, y, p)
$$
with the equality :
$$
\text{ind}_{=_{A}}(C, c,x, x,\text{refl}_{x}) = c(x_{0})
$$

---
# References
