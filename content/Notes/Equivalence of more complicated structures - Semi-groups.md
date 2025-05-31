---
tags:
  - Note
---
202505091805

Tags : [[Homotopy Type Theory]]
# Equivalence of more complicated structures - Semi-groups
---
Consider semi groups as defined in [[Semi Groups in Types Theory]]. Let $A$ be a semigroup and $B$ be another type. Loosely speaking, one can make the claim that a bijection between $2$ sets induces an isomorphic structure form one to another. With univalence it is in fact that straigthforward because $\text{Semi-Group-Str}$ is a type family, and therefore has an action on paths between types given by the transport.

$$
\text{transport}^{\text{Semi-Group-Str}}(\text{ua}(e)) : \text{Semi-Group-Str}(A) \to \text{Semi-Group-Str}(B)
$$
Now lets see what the transport does by considering the object $(m, a)$
$$
\text{transport}^\text{Semi-Group-Str}(m, a) = (m',a') 
$$
where $m'$ is the multiplication operation:
$$
\begin{align}
&m':B \to B \to B \\
&m'(b, b') :\equiv \text{transport}^{X \mapsto (X\to X \to X)}(\text{ua}(e), m)(b_{1}, b_{2})
\end{align}
$$
and $a'$ the induced proof of associativity
$$
\begin{align}
&a' : \text{Assoc}(B, m') \\
&a' :\equiv \text{transport}^{(X, m) \mapsto \text{Assoc}(X, m)}\big(\text{pair}^=(\text{ua}(e), \text{refl}_{m'}) \big)
\end{align}
$$
where $\text{Assoc}(A, *)$ is the type $\prod_{(x,y,z:A)} (x * y)*z = x*(y*z)$. and by function extensionality we only need to check what happens when an arbitrary $m'$ is applied on $b,b'$.  Any by applying 

[[Transport over a function between families]]

we have that $m'(b,b')$ is
$$
\begin{align}
\text{transport}^{X \mapsto X}(&\text{ua}(e),  \\
(&\text{transport}^{X \mapsto X}(\text{ua}(e)^{-1},b_{1} ),  \\
&\text{transport}^{X \mapsto X}(\text{ua}(e)^{-1}, b_{2})))
\end{align}
$$
But since $\text{ua}$ is simply the quasi inverse of $\text{transport}^{X \mapsto X}$ we have
$$
e(m(e^{-1}(b_{1}), e^{-1}(b)))
$$
Thus, given 2 elements of $B$ the induced multiplication sends them to $A$ using the equivalence $e$, multiplies them together and pushed them back to $B$.

Moreover the proof for associativity is
$$
\begin{align}
m'(m'(b_{1},b_{2}),b_{3}) &= e(m(e^{-1}(m'(b_{1}, b_{2})), e^{-1}(b_{3}))) \\
&=e(m(e^{-1}(e(m(e^{-1}(b_{1}), e^{-1}(b_{2})))), e^{-1}(b_{3})))\\
&=e(m(m(e^{-1}(b_{1}), e^{-1}(b_{2})), e^{-1}(b_{3})))\\
&=e(m(e^{-1}(b_{1}), m(e^{-1}(b_{2}), e^{-1}(b_{3}))))\\
&=e(m(e^{-1}(b_{1}), e^{-1}(e(m(e^{-1}(b_{2}), e^{-1}(b_{3})))) )) \\
&=e(m(e^{-1}(b_{1}), e^{-1}(m'(b_{2}, b_{3})) ))\\
&= m'(b_{1}, m'(b_{2}, b_{3}))
\end{align}
$$
Given that this is an algebraic structure, the proof for associativity seems weird, but the homotopy consider the types as general homotopy spaces, so we don't have a guarantee that it resprencs the semi-group structure.

---
# References
- [[Semi-Groups]]
- [[Semi Groups in Types Theory]]
- [[Transport]]
- [[Transport over a function between families]]