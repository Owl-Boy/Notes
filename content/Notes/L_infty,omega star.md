---
tags:
  - Note
  - Incomplete
---
202504272204

Tags : [[Finite Model Theory]]
# $\mathcal{L}_{\infty, \omega}^*$ 
---
$L_{\infty,\omega}^*$ is an extension to $\mathcal{L}_{\infty, \omega}$ which was discussed in [[FO with Infinitary Connectives]].

This is an extremely powerful logic $\mathcal{L}_{\infty, \omega}\text{(Cnt)}$ is extends $\mathcal{L}_{\infty, \omega}$ as follows:
>[!definition]
>Consider rules of $\mathcal{L}_{\infty, \omega}$ and add the following:
>- Each variable or constant of the second sort is a term of the second sort
>- If $\varphi$ is a formula and $\vec{x}$ is a tuple containing free first-sort variables in $\varphi$, then $\#\vec{x}.\varphi$ is a term of the second sort, and its free variables are those in $\varphi$ except those in $\vec{x}$. The interpretation is the number of tuples that satisfy $\varphi$.
>- $\exists ix \varphi$. Counting quantifier but $i$ is not bounded now.
>
>A Model of this logic looks like
>$$
>\langle \{ a_{1} \dots a_{n-1} \}, \mathbb{N}, (R_{i})^\mathfrak A, \{ k \}_{k\in \mathbb{N}} \rangle
>$$

This is too powerful and it can not only describe every property on structure, it can also define any relation on natural numbers.

We now restrict this logic by defining the rank for a formula in this logic. For this we will be ignoring the rank of the second sort and we inductively define it as follows:
>[!definition]
>- $\text{rk}(t)=0$ if $t$ is a variable or constant.
>- $\text{rk}(\varphi) = 0$ if this is an atomic formula of first kind.
>- $\text{rk}(t_{1} = t_{2}) = \max(\text{rk}(t_{1}), \text{rk}(t_{2}))$, where $t_{1}, t_{2}$ are terms
>- $\text{rk}(\lnot \varphi) = \text{rk}(\varphi)$
>- $\text{rk}(\#\vec{x}. \varphi) = \text{rk}(\varphi)+|\vec{x}|$.
>- $\text{rk}\left( \bigvee \varphi_{j} \right) = \text{rk}\left( \bigwedge \varphi_{j} \right) = \sup (\text{rk}(\varphi_{j}))$
>- $\text{rk}(\forall x, \varphi(x)) = \text{rk}(\exists x, \varphi(x))= \text{rk}(\exists ix, \varphi(x))=\text{rk}(\varphi)+1$
>- $\text{rk}(\forall i, \varphi) =\text{rk}(\exists i, \varphi) = \text{rk}(\varphi)$

We can now finally define $\mathcal{L}_{\infty, \omega}^*$ as follows:
>[!definition]
>$\mathcal{L}_{\infty,\omega}^*\text{(Cnt)}$ is the set of formulae in $\mathcal{L}_{\infty, \omega}\text{(Cnt)}$ that have a finite rank.

This logic is much weaker than the previous one, and is not closed under infinite disjunctions and conjunctions, but is powerful enough to contain counting logic extensions of $\text{FO}$. That is

>[!lemma]
>For each formula $\varphi$ with quantifier rank $k$ in $\text{FO}$ or $\text{FO(Cnt)}$, there is a formula $\phi$ of the same rank in $\mathcal{L}_{\infty, \omega}^*\text{(Cnt)}$ such that:
>$$
>\varphi(\vec{x}) \iff \phi(\vec{x})
>$$


---
# References
