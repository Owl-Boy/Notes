---
tags:
  - Note
---
202504032304

Tags : [[Homotopy Type Theory]]
# Based Path Induction
---

Another way to talk about [[Path Induction]] is that, given a proof, that uses $p: x=_{A}y$ then you can replace all instances of $x$ and $y$ with some unknown element $a:A$.

That motivates the equivalent second induction principle that can be used when one of the points is fixed.

>[!note] Based Path Induction
>Fix an element $a:A$ and let 
>$$
>C: \prod_{x:A} (a=_{A}x) \to \cal U
>$$
>be a family of types.
>Let $c$ be the element
>$$
>c:C(a, \text{refl}_{a}).
>$$
>Then there exists a function 
>$$
>f:\prod_{(x:A)}\prod_{(p: a=_{A}x)} C(a, x)
>$$
>such that
>$$
>f(a, \text{refl}_{a}):\equiv c
>$$

The based path induction states that given a family $C(x, p)$ where $x:A$ and $p: a=_{A} x$, for a fixed $a:A$, then to define it for all such $x$ and $p$. Then it is enough to define it for $a$ and $\text{refl}_{a}$.

As a function it becomes:
$$
\text{ind}_{=_{A}}': \prod_{(a:A)}\prod_{\left( C:\prod_{(x:A)}(a=x) \to\mathcal U \right)} C(a, \text{refl}_{a}) \to \prod_{(x:A)} \prod_{(p: a=_{A}x)} C(x, p)
$$
with the equality
$$
\text{ind}_{=_{A}}'(a, C, c, a, \text{refl}_{a}) = c
$$


---
# References

