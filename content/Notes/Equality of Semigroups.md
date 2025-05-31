---
tags:
  - Note
---
202505131505

Tags : [[Homotopy Type Theory]]
# Equality of Semigroups
---
The type $\text{Semi-Group}$ as defined in [[Semi Groups in Types Theory]] is the type of all Semigroups, consider $(A, m ,a)$ and $(B,m',a')$ which are both elements of $\text{Semi-Group}$. By [[Higher Groupoid Structure of Sigma Type]] we get that $(A,m,a)=_{\text{Semi-Group}}(B,m',a')$ is equal to the pair of paths
$$
\begin{align}
p_{1}&:A =_{\cal U} B \\
p_{2}&: \text{transport}^\text{Semi-Group}(p_{1},(m,a))=(m',a')
\end{align}
$$
By unvalence we cal say that $p_{1}=\text{ua}(e)$ for some equivalence $e:A\to B$. By 
what was figured out in [[Equivalence of more complicated structures - Semi-groups]] that $p_{2}$ can be given by the pair of proofs,first of which is
$$
\prod_{y_{1},y_{2}:B} e(m(e^{-1}(y_{1}), e^{-1}(y_{2})))=m'(y_{1},y_{2})
$$
Which by cancellation of inverse becomes the following
$$
\prod_{x_{1},x_{2}:A}e(m(x_{1},x_{2}))=m'(e(x_{1}),e(x_{2}))
$$
and this shows that the equality moves the multiplication operator across the equivalence $e$.

The other part shows that the equivalence induces the proof of associativity.

The conclusion is that semi-groups are equal, precisely when they are isomorphic as algebraic structures. And After doing some category theory here it is possible to show that all construction of mathematical structures respect isomorphisms.

---
# References
- [[Semi-Groups]]
- [[Higher Groupoid Structure of Sigma Type]]
- [[Equivalence of more complicated structures - Semi-groups]]
- [[Transport]]