---
tags:
  - Note
---
202503220603

Tags : [[Homotopy Type Theory]]
# Function Type
---
Given types $A$ and $B$, we can construct the type $A \to B$ of functions with domain $A$ and codomain $B$. Unlike set theory, where functions are defined as a special subset of the product set, here functions are a primitive concept.

So given an element $a: A$ and a function $f : A\to B$ we can apply the function to get $f\ a : B$. (the brackets for function application are generally omitted because lambda calculus is usually the language things are written in).

## Describing a Function
There are 2 ways to write functions:
- First is to write the definition with a name as follows
  $$f(x) : \Phi$$
  For this to be valid, one would have to check that assuming $x:A$ the expression on the rhs gives an element of type $B$ and hence the function is of the type $A \to B$
- The other way to write it is $\lambda$ abstraction
  $$(\lambda (x:A). \Phi):A\to B$$
  writing the type of the argument is generally omitted because it can be inferred from the type of the function, so the above can be written as
  $$(\lambda x. \Phi) : A \to B$$

Some notations for these are:
- $(x\mapsto \Phi) : A\to B$
- $g(x, -)$ which should be thought of as $\lambda y.g(x, y)$

>[!note]
>All functions have exactly 1 argument, so function with multiple arguments are represented by currying, to make the bracket scene less insane for named function definition we allow $f(x, y)$ instead of $f(x)(y)$ so we have 
>$$f(x, y) \equiv \Phi\quad \text{is the same as}\quad f\equiv \lambda x.\lambda y.\Phi$$

---
# References
