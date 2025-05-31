---
tags:
  - Note
aliases:
  - Sum Type
---
202503272003

Tags : [[Homotopy Type Theory]]
# Dependent Pair Types
---
*Dependent Sum Types* are [[Product Type(HoTT)|Product Types]] such that the type of the second element of the tuple is dependent on the first one.

This is also called the $\Sigma$-type because the set theory equivalent is disjoint union over some set.

Given $A:\cal U$ and a [[Universes#^ea1d66|family]] $B: A \to \cal U$, the dependent pair type is written as $\Sigma_{x:A}B(x)$.

To construct an element of this type we need a pair $(a, b):\sum_{x:A}B(x)$ such that $a:A$ and $b:B(a)$. It is clear to see that if the family is constant then this is just the pair type.

All constructions here are generalisation of those of product types

>[!note] Recursion Principle
>To define a function $f:\sum_{(x:A)}B(x) \to C$ one should provide a function $g:\prod_{(x:A)}B(x) \to C$ and the following description can be given to it:
>$$
>f((a, b)) :\equiv g(a)(b)
>$$

>[!example]
>We can now derive the projection maps for this type
>$$
>\text{pr}_{1}:{\huge(} \sum_{(x:A)}B(x) {\huge)} \to A
>$$
>And we define it as
>$$
>\text{pr}_{1}((a, b)) :\equiv a
>$$
>But since the type of the element depends on the first one, we need to define a dependent function

>[!note] Induction Principle
>For every function into the family $C:\left( \sum_{(x:A)}B(x) \right) \to \cal U$
>$$
>g:\prod_{a:A} \prod_{b:B(a)} C((a, b))
>$$
>we can define the function
>$$
>f:\prod_{p: \sum_{x:A}B(x)} C(p)
>$$
>by giving it the definition
>$$
>f((x, y)) :\equiv g(x)(y)
>$$

>[!example] Example cont.
>Now we can define the second projection which will have the following type:
>$$
>\text{pr}_{2} : \prod_{p:\sum_{x:A}B(x)}B(\text{pr}_{1}(p))
>$$
>with the following definition:
>$$
>\text{pr}_{2}((a, b)) :\equiv b.
>$$

We package the induction and recursion principle into the *recursor*:
$$
\text{rec}_{\sum_{x:A}B(x)}:\prod_{C:\cal U} \left( \prod_{x:A}B(x) \to C \right) \to \sum_{x:A}B(x) \to C 
$$
With the defining equation equation:
$$
\text{rec}_{\sum_{x:A}B(x)}(C, g, (a, b)) :\equiv g(a)(b)
$$
And we have the corresponding induction operator with type;
$$
\text{ind}_{\sum_{x:A}B(x)} : \prod_{C:\sum_{x:A}B(x) \to \cal U} \left( \prod_{a:A} \prod_{b:B(a)} C(a,b) \right) \to \prod_{p:\sum_{x:A}B(x)}C(p)
$$
with the defining equation
$$
\text{ind}_{\sum_{x:A}B(x)}(C,g, (a, b)) :\equiv g(a)(b)
$$

---
# References
[[Product Type]]