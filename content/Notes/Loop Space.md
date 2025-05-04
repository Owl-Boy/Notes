---
tags:
  - Note
---
202505030005

Tags : [[Homotopy Type Theory]]
# Loop Space
---
>[!definition]
>The Loop Space of a point $a:A$ for some type $A$, which is generally written as $\Omega(A, a)$ is the type $a =_{A}a$. This type follows an $\infty$-group structure.

We will also be consider higher group spaces, that is group spaces of group spaces and so one, for example:
- $\Omega^2(A, a)$ is defined as $\text{refl}_{a}=_{(a=_{A}a)} \text{refl}_{a}$ and so on.

Since all paths on the space have the same starting and end point, Concatenation becomes the group operation and has the type:
$\Omega(A,a) \times \Omega(A, a) \to \Omega(A, a)$.

Given a [[Pointed Type]] $(A, a)$ we define its loop space as the following pointed type:
$$
\Omega(A, a) = ((a=_{A}a), \text{refl}_{a})
$$
and we can define its higher loops spaces as follows:
$$
\begin{align}
\Omega^0(A, a) &:\equiv (A, a) \\
\Omega^{n+1}(A,a) &:\equiv \Omega^n(\Omega(A, a))
\end{align}
$$

---
# References
