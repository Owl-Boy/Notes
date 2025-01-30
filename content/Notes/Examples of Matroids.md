---
tags:
  - Note
---
202501291901

Tags : [[Topics in Algorithms]]
# Examples of Matroids
---
## Uniform matroid $U_{k,n}$
$I=\{ X\subseteq E\mid |X|\leq k \}$ for a given $k$.
$U_{n,n}$ is known as the *free matroid*.

## Partition matroid
$E=E_{1}\dot{\cup}E_{2}\dot{\cup}\dots \dot{\cup}E_{l}$
$E_{1},\dots,E_{l}$ is a partition of $E$.
Integers $k_{1},\dots ,k_{l}$ as input.
$I=\{ X\subseteq \mid |X\cap E_{i}|\leq k_{i}, i\in[l] \}$

> [!note] 
> Observe that if the sets overlap, then $I$ is not a matroid because we can have $|X|<|Y|$, but $X$ could have all the constraints tight as one element can then contribute to multiple constraints.

## Linear matroid
Matrix $A_{m\times n}$, columns $A_{1},\dots,A_{n}$.
$I=\{ X\subseteq[n]\mid \text{Colums corresponding to }X\text{ are linearly independent} \}$
The matrices could be over $\mathbb{F}_{2}$ or $\mathbb{F}_{3}$.

---
# References
