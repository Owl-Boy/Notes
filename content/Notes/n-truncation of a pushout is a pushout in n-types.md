---
tags:
  - Note
  - Incomplete
---
202509222009

Tags : [[Homotopy Type Theory]]
# n-truncation of a pushout is a pushout in n-types
---
>[!theorem]
>Let $\cal D$ be a span and $(D, c)$ be its pushout. Then $(\|D\|_{n},\|c\|_{n})$ is a pushout of $\|\cal D\|_{n}$ in $n$-types.

To show this, we need to show that this satisfies the universal property of pushouts.

Consider the following diagram where $E$ is an $n$-type
![[Pasted image 20250922203637.png]]

The upper horizontal arrow is an equivalence since $E$ is an $n$-type.
The right, downwards arrow is an equivalence since $c$ is a pushout.

by the 2 out of 3 property, we need to show that the middle horizontal arrow is an equivalence and the upper square commutes to show that the left downward arrow is an equivalence.

To show that the upper square commutes:
$$
\begin{align}
(t\circ\|c\|_{n})\circ |-|_{n}^{\cal D} &= t\circ(\|c\|_{n}\circ |-|_{n}^{\cal D}) \\
&= t\circ (|-|_{n}^D \circ c) \\
&= (t\circ|-|_{n}^D)\circ c
\end{align}
$$
The last line is by functoriality of truncations, the first equality if by the theorem proved in [[Maps between Cocones]].

Now we need to show that the middle horizontal arrow is an equivalence, for that, we look at the bottom square. Both vertical arrows are equivalence as they are just an application of $\text{happly}$. And now we are only left to show that the bottom arrow is an equivalence:
$$
(i, j, p) \longmapsto (i\circ |-|_{n}^A,j\circ |-|_{n}^B, q)
$$
we have that the lower square commutes definitionally on the first two components.

So we need to show that $q$ is equal to:
$$
\begin{align}
i(|f(z)|_{n})&= i(\|f\|_{n}(|z|_{n})) \\
&=j(\|g\|_{n}(|z|_{n})) \\ 
&=j(|g(z)|_{n})
\end{align}
$$
This is trivial, so by 2 out of 3 rule, the lower arrow is an equivalence, so the lower square commutes, so the middle horizontal arrow is an equivalence and the upper square commutes so the left downward arrow is an equivalence, and we are done.

---
# References
- [[Pushouts (HoTT)]]
- [[Pushouts of n-types]]
- [[n-Types]]
- [[Maps between Cocones]]