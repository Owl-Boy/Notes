---
tags:
  - Note
---
202505192305

Tags : [[Homotopy Type Theory]]
# Contractible Types
---
>[!definition]
>A type $A$ is called **Contractible** or a **Singleton** if there is an $a:A$, called the **Center of Contraction**, such that for all $x:A$ we have $a=x$. We done the specified path by $\text{contr}_{x}$.

We can also state it with the type $\text{is-Contr}$ defined as follows:
$$
\text{is-Contr}(A) :\equiv \sum_{a:A} \prod_{x:A} a=x
$$
>[!lemma]
>For a type $A$, the following are logically equiavlent:
>- $A$ is contractible
>- $A$ is a mere proposition, and there is a point $a:A$
>- $A$ is equivalent to the type $\mathbf{1}$

>[!note]
>It is interesting to see that the definition sounds more similar to the notion of path connectedness rather than contractibility, but maps are natural over equality, so two elements being equal gives a homotopy between the paths that connect it to the center.




---
# References
- [[Identity Type]]
- [[Some Contractible Types]]