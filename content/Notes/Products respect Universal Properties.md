---
tags:
  - Note
---
202505131605

Tags : [[Homotopy Type Theory]]
# Products respect Universal Properties
---
Given types $X,A,B$ we have a function
$$
(X \to A\times B) \to (X \to A) \times (X \to B)
$$
which is $f \to (\text{pr}_{1} \circ f, \text{pr}_{2}\circ f)$.
>[!lemma]
>The above function is an equivalence

Given functions  $(g,h)$ we send it to $\lambda x.(g(x),h(x))$. And we use this function to build the quasi-inverse so we need to show:
$$
(\text{pr}_{1}(f(x)),\text{pr}_{2}(f(x))) = f(x)
$$
we can show for each $x$ by [[Higher Groupoid Structure of Cartesian Product]] and this by function extensionality we get an equivalence.

For the other direction we have to show that the pair of functions $(g,h)$ becomes $(\lambda x. g(x), \lambda x.h(x))$ which is judgementally equal.

The above also holds for dependent functions
$$
\left( \prod_{x:X}A(x) \times B(x) \right) \to \Big( \prod_{x:X}A(x) \Big) \times \Big( \prod_{x:X}B(x) \Big)
$$
is an Equivalence. The proof is the same.

---
# References
[[Products and Coporducts]]
[[Universal Property (Riehl)]]
[[Higher Groupoid Structure of Cartesian Product]]