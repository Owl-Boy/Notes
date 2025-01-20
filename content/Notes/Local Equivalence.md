---
tags:
  - Note
---
202501191501

Tags : [[Finite Model Theory]]
# Local Equivalence
---
>[!definition] 
>Let $\frak A, B$ be $\sigma$-structures. Let $\vec{a}\in A^n$ and let $\vec{b}\in B^n$ We then write.
>$$(\mathfrak A, \vec{a}) \leftrightarrows_{d} (\mathfrak B, \vec{b})$$
>if there exists a bijection $f: A\to B$ such that for every $c\in A$,
>$$
>N_{d}^\mathfrak A(\vec{a}, c) \cong N_{d}^\mathfrak B(\vec{b}, f(c)).
>$$
>
>For the special case where $n=0$,  we simply write it as 
>$$
>N_{d}^\mathfrak A(c) \cong N_{d}^\mathfrak B(f(c)), \text{ for all } c\in A.
>$$

The above defined $\leftrightarrows_{d}$ relation states that there is intuitively a "local bijection" between the structures $\frak A, B$. The local isomorphism here is $f$, i.e it states that for every element $f$, the [[Neighborhood (Finite Model Theory)|neighborhood]] of $c$ is in bijection with the neighborhood of $f(c)$. The lemmas below summarized the property.

>[!lemma]
>1. $(\mathfrak A, \vec{a}) \leftrightarrows_{d} (\mathfrak B, \vec{b}) \implies |A| = |B|$.
>2. $(\mathfrak A, \vec{a}) \leftrightarrows_{d} (\mathfrak B, \vec{b}) \implies (\mathfrak A, \vec{a}) \leftrightarrows_{d'} (\mathfrak B, \vec{b}), \forall d' \leq d$
>3. $(\mathfrak A, \vec{a})\leftrightarrows (\mathfrak B, \vec{b}) \implies N_{d}^\mathfrak A(\vec{a}) \cong N_{d}^\mathfrak B (\vec{b})$



---
# References
