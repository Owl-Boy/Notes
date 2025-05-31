---
tags:
  - Note
---
202505251805

Tags : [[Homotopy Type Theory]]
# Contractible Fibers
---
The proof about $\text{ishae}$ used the fact that [[Fibers of Half Adjoint Equivalences are Contractible]]. Turns out this is a sufficient definition for equivalence.
>[!definition]
>A map $f:A\to B$ is called **Contractible** if for all $y:B$, the fiber of $\text{fib}_{f}(y)$ is contractible.

Hence we define:
$$
\text{is-Contr}(f) :\equiv \prod_{y:B} \text{is-Contr}(\text{fib}_{f}(b))
$$
In general, we will say that a map has a property if all its fibers have the property, which is standard in homotopy theory according to the book.

We have already shown $\text{ishae}(f) \to \text{is-Contr}(f)$ in [[Fibers of Half Adjoint Equivalences are Contractible]], we now need to show the other direction:
>[!lemma]
>For any $f:A\to B$ we have $\text{is-Contr}(f)\to\text{ishae}(f)$.

Let $P:\text{is-Contr}(f)$ we will send each $b:B$ to the center of contraction of the fiber using the function $g:B \to A$:
$$
g(y) = \text{pr}_{1} ( \text{pr}_{1}(y))
$$
We can simply use the homotopy given here to create $\epsilon$
$$
\epsilon(y) :\equiv \text{pr}_{2}(\text{pr}_{1}(y))
$$
For the other two, we simple need a definition for the correct [[Coherence Types for Equivalences]], that is $\text{rcoh}_{f}(g, \epsilon)$. But that is equivalent to giving a path from $(gfx, \epsilon(fx))$ to $(x, \text{refl}_{x})$ in the fiber of $f$ over $fx$ for each $x$.
But we have that as fiber of $fx$ is contractible by hypothesis. 

We also have 2 simple lemmas:
>[!lemma]
>$\text{is-Contr}(f)$ is a mere proposition

Since $\text{is-Contra}(A)$ is a mere proposition and [[Some Type Formers respect Mere Propositions]], we are done.

>[!lemma] Corollary
>$\text{is-Contra}(f)\simeq\text{ishae}(f)$

>[!lemma] Corollary
>If $f:A\to B$ and $B\to\text{isequiv}(f)$, then $f$ is an equivalence.

We just need to show that fibers of $f$ are contractible, but we have $e:B\to\text{isequiv}(f)$.
Given $b:B$ we get $e(b)$, which proves that $\text{fib}_{f}(b)$ is contractible, so we are done.

---
# References
- [[Fibers (HoTT)]]
- [[Fibers of Half Adjoint Equivalences are Contractible]]
- [[Coherence Types for Equivalences]]
- [[Some Type Formers respect Mere Propositions]]