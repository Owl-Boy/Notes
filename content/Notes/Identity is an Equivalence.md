---
tags:
  - Note
---
202505022305

Tags : [[Homotopy Type Theory]]
# Identity is an Equivalence
---
**Equality** of all things should be an equivalence relation. But in the definition of [[Identity Type]], we only require reflexivity.

Turns our that symmetry and transitivity of identity can actually be proven!!

>[!theorem]
>For every type $A$ and elements $x, y:A$, there is a function:
>$$
>f:x = y \to y = x
>$$
>denote $p \mapsto p^{-1}$, such that $\text{refl}_{x} \equiv \text{refl}_{x}^{-1}$ for any $x:A$.
>
>We call $p^{-1}$ the inverse of $p$.

We want to construct the inverse $p^{-1}$:
- For every type $A$
- Every pair of elements $x, y:A$
- Every witness of the equality $p$.

By induction, it suffices to prove the case when $y$ is $x$ and $p$ is $\text{refl}_{x}$. But in that scenario, both the domain and range of the function is $x=x$, so we can simply define the function to be $\text{id}_{A}$.

>[!theorem]
>For every type $A$ and elements $x, y, z:A$ there is a function of types:
>$$
>(x=y) \to (y= z) \to (x=z)
>$$
>written as $p \mapsto q \mapsto p \cdot q$ such that $\text{refl}_{x} \cdot \text{refl}_{x} \equiv \text{refl}_{x}$ for any $x:A$.
>
>We call $p \cdot q$ the concatenation of $p$ and $q$.

Say the inputs are $p$ and $q$, we first do path induction on $p$, that would turn the first argument to $\text{refl}_{x}$ and the type of the function becomes $(x=z)\to (x=z)$. We now apply path induction on $q$, and we get that the type becomes $(x=x)$ that we have an element of, that is $\text{refl}_x$.

---
# References
