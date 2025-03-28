---
tags:
  - Note
---
202503272203

Tags : [[Homotopy Type Theory]]
# Sum Types
---
Given types $A, B:\cal U$ we introduce the type $A+B$ which is the disjoint union in set theory. This must be a fundamental construct because there is no notion of union of types in type theory. We also define a unit type for this operation that we will call $\mathbf{0}:\cal U$, the empty type.

There are 2 constructors of the type $A+B$:
- $\text{inl}:A \to A+B$
- $\text{inr}:B\to A+B$
These are called "left injection" and "right injection".

There are no ways to construct elements of the empty type.

>[!note] Recursion Principle
>To construct a non-dependent function $f:A+B \to C$ one needs 1 functions of type $g_{0}:A\to C$ and $g_{1}:B\to C$ respectively, now we can define $f$ as:
>$$
>\begin{align}
>f(\text{inl}(a)) & :\equiv g_{0}(a)\\
>f(\text{inr}(b)) & :\equiv g_{1}(b)
>\end{align}
>$$
>
>That is, the function is defined by case-analysis and the recursor has the type:
>$$
>\text{rec}_{A+B} : \prod_{C:\cal U}(A\to C) \to (B\to C) \to A+B \to C
>$$
>with defining equation
>$$
>\begin{align}
>\text{rec}_{A+B}(C,g_{0}, g_{1},\text{inl}(a)) :\equiv g_{0}(a)\\
>\text{rec}_{A+B}(C,g_{0}, g_{1},\text{inr}(b)) :\equiv g_{1}(b)
>\end{align}
>$$
>
>The recursor for $\mathbf{0}$ will have the type:
>$$
>\text{rec}_{\mathbf{0}}:\prod_{C:\cal U} \mathbf{0} \to C
>$$
>This can be constructed without giving any definition as $\mathbf{0}$ does not have any elements.

>[!note] Induction Principle
>To construct a dependent function out of a sum type, we assume we are given the family $C:A+B \to \cal U$ , then we require 2 functions:
>- $g_{0}:\prod_{a:A}C(\text{inl}(a))$
>- $g_{1}:\prod_{b:B}C(\text{inr}(b))$
>this gives the following definition for $f$:
>$$
>\begin{align}
>f(\text{inl}(a)) :\equiv g_{0}(a) \\
>f(\text{inr}(b)) :\equiv g_{1}(b)
>\end{align}
>$$
>
>Packaging the above construction into the induction operator we get
>$$
>\text{ind}_{A+B} : \prod_{C:A+B \to U}\left( \prod_{a:A}C(\text{inl}(a)) \right) \to \left( \prod_{b:B}C(\text{inr}(b)) \right) \to \prod_{x:A+B}C(x)
>$$
>
>And there is also an induction operator on the emtpy that has the type:
>$$
>\text{ind}_{\mathbf{0}} : \prod_{C:\mathbf{0}\to\cal U}\prod_{z:\mathbf{0}}C(z)
>$$




---
# References
