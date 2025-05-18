---
tags:
  - Note
  - Incomplete
---
202505061405

Tags : [[Homotopy Type Theory]]
# Higher Groupoid Structure of Pi Type
---
Given a type $A$ and a family $B:A \to\cal U$ over it, consider the function type $\prod_{(x:A)}B(x)$. We would like to have the type $f=g$ of paths to be equivalent to pointwise paths as follows:
$$
(f=g) \simeq \left( \prod_{x:A}f(x)=_{B(x)}G(x) \right)
$$
For a set theory pov, it says 2 functions are equal if for each inputs, their outputs are equal. From a topological perspective, paths in function spaces are just continuous homotopes. From a category pov says isomorphisms in function category are a natural family of isomorphisms.

Type Theory typically is only able to prove this in 1 direction, fairly easily by path induction:
$$
\text{happly}: (f=g) \to \left( \prod_{x:A}f(x)=_{B(x)}g(x) \right)
$$

Hence for now we shall assume the following:
>[!Theorem] Axiom 
>For any $A, B, f, g$ we have that $\text{happy}$ is an equivalence, and the inverse is given by:
>$$
>\text{funext}: \left( \prod_{x:A}f(x)=_{B(x)}G(x) \right) \to (f=g)
>$$

Also referred to as *function extensionality*.

We can consider $\text{funext}$ as an introduction rule and $\text{happly}$ as an elimination rule with the following computation rule
$$
\text{happly}(\text{funext}(h), x) = h(x)
$$
along with:
$$
p = \text{funext}(x \mapsto\text{happly}(p, x))
$$
All of this also applies to non-dependent functions as they are a special case of functions.

Given a type $X$ and $x:X$ and families $A,B: X \to \cal U$, $p:x_{1} =_{X} x_{2}$ and $f: A(x_{1}) \to B(x_{1})$ we have 
$$
\text{transport}^{A \to B}(p, f) = x \mapsto \text{transport}^B(p, f(\text{transport}^A(p^{-1}, x)))
$$

^7ee656

To justify this, see that we are given a function $f:A(x_{1})\to B(x_{1})$, so we want a function $p_{*}(f): A(x_{2}) \to B(x_{2})$, for that assume we are given an $x : A(x_{2})$, We then transport to get an element of $A(x_{1})$, then we apply $f$ to get an element of $B(x_{1})$, then we transport it again to get an element of $B(x_{2})$.
Also here the the type family $A\to B$ is $x\mapsto A(x) \to B(x)$.

The exact same idea works in teh dependent case, but the function it self is significantly more ugly:
![[Pasted image 20250506162144.png]]
with the definitions
![[Pasted image 20250506162158.png|450]]


---
# References
