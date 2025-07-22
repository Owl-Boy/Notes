---
tags:
  - Note
---
202506171106

Tags : [[Homotopy Type Theory]]
# W-Types
---
$W$-types are the type of **Well Founded Trees**.  These trees represent the structure of most inductive data-types.

>[!definition] Formation Rule
>The description of a $W$-type requires a type $A:\cal U$ and $B:A \to \cal U$ to get the type $W_{a:A}B(a)$.
>- The Type $A$ is supposed to be a type that indexes constructors
>- The Type $B(a)$ is supposed to represent the arity of the constructor labelled by $a$.
>For the construction, for each $B(a)$, there is a function $f:B(a)\to W_{a:A}B(a)$ and the place where an element $b:B(a)$ is mapped to is supposed to be the $b^\text{th}$ argument of the constructor.

Here are some [[Examples for W-Types]].

>[!definition] Construction Rule
>The $W$-Type is an [[Inductive Types]] with the following constructor:
>$$
>\text{sup}:\prod_{a:A}\Big(B(a) \to W_{a:A}B(a)\Big) \to W_{a:A}B(a) 
>$$
>This constructor takes a label $a$, then takes a collection of element of $W_{a:A}B(a)$ as a function $B(a)\to W_{a:A}B(a)$ and puts them together to give an element $W_{a:A}B(a)$.

For the elimination rule, we want it too look like structural induction, to prove something for all elements of $W_{a:A}B(a)$, we need to show:
- For each constructor, it holds for all arguments of the constructor, and that it holds for the element constructed with those arguments and constructor.
- A special case for that would be the base one, where the constructor has no arguments, so we get the following induction principle.

>[!note] Induction Principle
>To construct an element of type $\prod_{x:W_{a:A}B(a)}E(x)$ we only need to construct the element:
>$$
>e:\prod_{(a:A)}\prod_{(f:B(a) \to W_{x:A}B(x))}\prod_{( g:\prod_{b:B(a)} E(f(b)))}E(\text{sup}(a, f))
>$$
>The first one picks a constructor. The second one pics arguments of the constructor, the third one proves the statement for the arguments, and the final output proves the statement for the constructed element.

For functions on a $W$-type, one can also make a similar argument as [[Uniqueness of functions created using induction principle]]. This is a very general version of the statement and proves it for a lot of inductive types.

>[!theorem]
>Let $g,h:\prod_{x:W(a:A)B(a)}E(x)$ be two functions which satisfy the recurrence:
>$$
>e:\prod_{a, f}\left( \prod_{b:B(a)} E(f(b)) \right) \to E(\text{sup}(a, f))
>$$
>such that:
>$$
>\begin{align}
>\prod_{a, f}g(\text{sup}(a, f)) &= e(a, f, \lambda b.g(f(b)))\\
>\prod_{a, f}h(\text{sup}(a, f)) &= e(a, f, \lambda b.h(f(b)))
>\end{align}
>$$
>Then $f, g$ are equal.

---
# References
- [[Inductive Types]]
- [[Similar description of inductive types lead to equal types]]
- [[Uniqueness of functions created using induction principle]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Examples for W-Types]]
- [[Double on Natural Numbers using W-Types]]