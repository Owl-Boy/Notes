---
tags:
  - Note
---
202501211501

Tags : [[Finite Model Theory]]
# Local Equivalence  Lemma 1
---
>[!lemma] 
>If $\mathfrak A \leftrightarrows_{d}\mathfrak B$ and $\vec{a} \approx_{3d + 1} \vec{b}$, then $(\mathfrak A, \vec{a})\leftrightarrows_{d}(\mathfrak B, \vec{b})$.

To prove requires a construction $f:A \to B$ such that every $(\vec{a}, c) \approx_{d} (\vec{b}, f(c))$, for every $c \in A$.

Let $g: A \to B$ be the bijection that witnesses $\mathfrak A \leftrightarrows_{d} \mathfrak B$. And let $h: N_{3d+1}^\mathfrak A(\vec{a}) \to N_{3d+1}^\mathfrak B(\vec{b})$ the isomorphism that witnesses $\vec{a} \approx_{3d+1} \vec{b}$, as in the following diagram.

>[!todo] Draw the diagram

Let $X$ be the ball of size $2d+1$ around $\vec{a}$ and let $Y$ be a ball of size $2d+1$ around $\vec{b}$. And We define $f|_{X}=h$. Since $\vec{a} \approx_{3d+1} \vec{b}$, for any $c\in X$, the ball of size $d$ around $c$ is isomorphic to ball of size $d$ around $h(c)$, hence $f(c)$.

For all $c\in A$, $g$ takes a ball around $c$ to a ball that is of the same [[Isomorphism Types of Models|isomorphism type]] as $c$. Given any isomorphism type $\tau$ let $A_{\tau}$ be the set of points such that a ball around them of radius $r$ has isomorphism type $\tau$. Let $B_{\tau}$ be the image of $A_{\tau}$ under $g$, Therefore $B_\tau$ is in bijection with $A_{\tau}$.

Also $h$ forms a similar bijection of points in $X$ and $Y$, hence $A_{\tau}$ and $B_{\tau}$ restricted to $X$ and $Y$ are also in bijection, and are both finite sets.

Hence $A_{\tau} \setminus X$ is in bijection with $B_{\tau}\setminus Y$. Now we can define $g'$ on this that takes a point $p$ to a corresponding point $q$ such that the balls around $p$ and $q$ of radius $d$ are of the same isomorphism type.

We define $f$ to be $g'$ outside of $X$ such that $N_{d}^\mathfrak A(\vec{a}, c) \cong N_{d}^\mathfrak B(\vec{b}, f(c))$. So we have $(\mathfrak A, \vec{a}) \leftrightarrows_{d} (\mathfrak b, \vec{b})$

---
# References