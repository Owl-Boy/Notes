---
tags:
  - Note
---
202503220703

Tags : [[Homotopy Type Theory]]
# Dependent Function Type
---
A **Dependent Function Type**, (also called a $\Pi$-type) is a generalization of the standard [[Function Type]].

An element of a $\Pi$-type is a function whose co-domain can be dependent on the input.

>[!definition]
>Given a type $A:\mathcal U$ and a family $B : A \to \mathcal U$, we may construct the type of dependent function $\prod_{x:A}B(x):\mathcal U$

>[!tip]
>If $B$ is the constant family, then the dependent type $\prod_{x:A}B(x)$ is simply the normal function type $A \to B$.

## Polymorphic Functions
A polymorphic function is one which takes a type as one of its arguments and then acts on elements of the type (or other types constructed from it).

An example of a polymorphic function is $\text{Id}: \prod_{A:\mathcal U}A\to A$ which can be defined by $\text{Id} :\equiv \lambda(A:\mathcal U).\lambda(x:A).x$

Again, our notation is loose enough that we sometimes omit things that can be inferred, example $\text{Id}(a)$ for some element $a:A$ lets us infer that the first argument was the type $A:\mathcal U$.

## More notation
Consider the following example
>[!example] Swap Function
>The swap function takes in a function with 2 inputs (curried ofc) and swaps the order in which the function takes in those inputs, it belongs to the type
>$$
>\prod_{A:\mathcal U}\; \prod_{B:\mathcal U}\; \prod_{C:\mathcal U} (A \to B \to C) \to (B \to A \to C)
>$$
>And this can be defined as
>$$
>\text{swap}(A, B, C, g) :\equiv \lambda b .\lambda a.g\ a\ b
>$$

Note that in general the order is important because an argument's type can depend on that of the previous argument, but when that is not the case, like the for $\text{swap}$, one can write the type as follows
$$
\text{swap} : \prod_{A, B, C :\mathcal U} (A \to B \to C) \to (B \to A \to C)
$$

---
# References
- [[Universes]]
- [[Function Type]]