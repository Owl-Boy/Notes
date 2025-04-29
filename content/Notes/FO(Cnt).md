---
tags:
  - Note
aliases:
  - FO with Counting
---
202504272004

Tags : [[Finite Model Theory]]
# $\text{FO(Cnt)}$
---
$\text{FO(Cnt)}$ is a extensions of [[First Order Logic|FO]] that allows a new sort of quantification which is meant to allow $\text{FO}$ to be able write statements about cardinalities and counts, the *counting quantifier* looks like the following:
$$
\exists ik\; \varphi(x)
$$
This line reads as "There are at least $i$ elements $a:A$ such that $\varphi(a)$ holds".

Note that the quantified variable $i$ is a natural number does not belong to $A$, it is of a different "sort". There also needs to be some arithmetic operators available for this to be useful. But first the definition:

>[!definition]
>Given a vocabulary $\sigma$, a $\sigma$-structure for $\text{FO}$ with counting, $\text{FO(Cnt)}$, is a structure of the form:
>$$
>\langle \{ a_{0}\dots a_{n-1} \}, \{ 0 \dots n-1 \}, (R_{i})^\mathfrak A, +, \times, \underline{\min}, \underline{\max}\rangle
>$$
>Such that $\langle \{ a_{0} \dots a_{n-1} \}, (R_{i})^\mathfrak A \rangle$ is a $\sigma$-structure for $\text{FO}$. 
>
>$+$ and $\times$ are ternary relations on the elements of the second sort representing addition and multiplication while $\underline{\max} = n-1$ and $\underline{\min}=0$ .
>This also extends rules of $\text{FO}$ as follows: 
>- $\underline{\min}$ and $\underline{\max}$ and second sort quantified variables are all terms of the second sort.
>- If $t_{1},t_{2},t_{3}$ are elements of the second sort then $+(t_{1},t_{2},t_{3})$ and $\times(t_{1},t_{2},t_{3})$ are formulae
>- If $\varphi(\vec{x}, \vec{i})$ is a formula, then $\exists i\  \varphi(\vec{x}, \vec{i})$ is a formula. This quantification binds the second sorted variable.
>- If $\varphi(y, \vec{x}, \vec{i})$ is a formula then $\phi(\vec{x}, i, \vec{i})=\exists iy\ \varphi(y, \vec{x}, \vec{i})$ is a formula. This quantification only bounds the variable of the first sort.
>  
>The following make the semantics, which only needs to be defined for the last term:
>$$
>\mathfrak A \vDash \psi(\vec{x}, i, \vec{i})\quad \text{ iff } \quad \Big| \big\{ b \in \{ a_{0}, \dots a_{n-1} \} :\!\!|\!\!: \mathfrak A \vDash \varphi(b, \vec{a}, \vec{i})\big\}\Big| \geq i
>$$



---
# References
