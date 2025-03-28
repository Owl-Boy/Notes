---
tags:
  - Note
---
202503271903

Tags : [[Homotopy Type Theory]]
# Product Type
---
Given types $A, B :\cal U$, we introduce the type $A \times B : \cal U$, which we will call the **cartesian product**. (formation).

Along with that we use the type that will be the unit for this product $\mathbf{1}: \cal U$. Also called the unit type with the only value in it denoted as $\star : \mathbf{1}$ 

Unlike set theory, ordered pairs are primitive to the theory.

>[!note] Elements
>We construct the pairs is obvious, given elements $a : A$ and $b:B$ one can construct $(a, b) : A \times B$. (construction of element).

We define equality such that it behaves like the elements of the type are pairs, so it is pairwise equal, which will be formalized later.

To describe a non-depended function $f : A\times B \to C$, since we know that such a function will be applied to elements of the form $(a, b)$ we say that for any function $g: A\to B \to C$, there is a function $f:(A \times B) \to C$ such that
$$
f\ ((a, b)) :\equiv g\ (a)\ (b)
$$
(elimination)

>[!note] Recursion Principle
>In set theory, we justify defining such a function by showing that the type only contains pairs hence it is okay to define a function on types. Here we assume that the function $f$ is well defined on all values from the start, using that we can show that $f$ contains pairs using the following functions
>$$
>\begin{align}
>\text{pr}_{1} &: A \times B \to A \\
>\text{pr}_{2} &: A \times B \to B
>\end{align}
>$$
>And defining them as 
>$$
>\begin{align}
>\text{pr}_{1} (a, b) &:\equiv a\\
>\text{pr}_{2} (a, b) &:\equiv b
>\end{align}
>$$
>
>Apart from the elimination principle, we also define the following function so that we don't need to invoke the function again and again:
>$$
\text{rec}_{A \times B} : \prod_{C:\cal U} (A \to B \to C) \to A\times B \to C
>$$
>with the definition
>$$
>\text{rec}_{A\times B}(C, g, (a, b)) :\equiv g(a)(b)
>$$
>. We call $\text{rec}_{A \times B}$ as the *recursor* of $A, B$.
>
>There is also a *recursor* for the unit type:
>$$
>\text{rec}_{\mathbf{1}} : \prod_{C:\cal U} C \to \mathbf{1} \to C
>$$
>And is given a definition by 
>$$
>\text{rec}_{\mathbf{1}}(C, c, \star) :\equiv c
>$$
>This is pretty useless.

For defining a dependent function $f : \prod_{x : A \times B}C(x)$ we provide a function $g:\prod_{a:A} \prod_{b:B}C((a, b))$.

Now we can formalise the uniqueness principle as a proposition, which is possible in this case:
$$
\text{uniq}_{A\times B}:\prod_{x:A\times B} (\text{pr}_{1}(x), \text{pr}_{2}(x)) =_{A\times B} x
$$

And we can also prove that $\text{uniq}_{A\times B}(x) \equiv \text{refl}_{x}$.

>[!note] Induction Principle
>Product types are also inductive types (non-atomic types defined using induction), they happen to be a degenerate case. In general it means that if a one want to prove a property for all elements, they only need to prove it for the generators, ordered pairs in this case. We give it the following type:
>$$
>\text{ind}_{A\times B} : \prod_{C:A\times B \to \cal U} \left( \prod_{x:A} \prod_{y:B} C((x, y)) \right) \to \prod_{x:A\times B} C(x) 
>$$
>And this can be given the following definition
>$$
>\text{ind}_{A\times B}(C, g, (a, b)) :\equiv g(a)(b)
>$$
>Induction principle describes how one is supposed to define a dependent function, so is also often called the *dependent eliminator*
>
>There is also an induction principle for the unit type, it has the following type
>$$
>\text{ind}_{\mathbf{1}} : \prod_{C:\mathbf{1} \to \cal U} C(\star) \to \prod_{x:\mathbf{1}}C(x)
>$$
>This can be used to define the uniquenss type for $\mathbf{1}$:
>$$
>\text{uniq}_{\mathbf{1}} : \prod_{x:\mathbf{1}}x=\star
>$$ 
>Along with the definition
>$$
>\text{uniq}_{\mathbf{1}}(x) :\equiv \text{refl}_{\star}
>$$

---
# References
[[Specifying a Type]]