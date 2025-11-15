---
tags:
  - Note
---
202510130110

Tags : [[Parameterized Algorithms]]
# Sunflower Lemma
---
>[!definition]
>A **sunflower** with $k$ petals and a core $Y$ is a collection of sets $\{ S_{1},S_{2}\dots S_{k} \}$ such that for all $i \neq j$ the intersection $S_{i} \cap S_{j}$ is exactly $Y$.

Note that $Y$ can be empty.

>[!lemma]
>Let $\mathcal A$ be a family of sets over a universe $U$, such that each in $\mathcal A$ has cardinality at exactly $d$. If $|\mathcal A|>d!(k-1)^d$ then $\mathcal A$ contains a sunflower with $k$ petals, and such a sunflower can be computed in time polynomial in $|\mathcal A|$, $|U|$ and $k$.

The construction is recursive:
- Given a family of sets $\mathcal A$, we first find an inclusion maximal sub-family of pairwise disjoint sets, which we call $\mathcal G=\{ S_{1},\dots S_{l} \}$, which can be done greedily.
- If we have that $l\geq k$ we get a family of disjoint petals, otherwise we know that each set in $\mathcal A$ intersects with some set in $\mathcal G$, in particular, each set intersects with $S=\bigcup\mathcal G$.
- We know that the size of the set is at most $d(k-1)$, hence we can find a subfamily $\mathcal A'$ of $\mathcal A$ that all intersect $S$ at the same point of size
  $$
  \frac{|A|}{|S|}> \frac{d!(k-1)^d}{d(k-1)} = (d-1)!(k-1)^{d-1}
  $$
- Let $u$ be the common element in all sets of $\mathcal A'$. We will now remove $u$ from all sets in $\mathcal A'$ to create the set $\mathcal A''$ which has at least $(d-1)!(k-1)^{d-1}$ sets of size exactly $d-1$, thus by induction hypothesis, we have a flower $\{ S_{1}',S_{2}'\dots S_{k}' \}$, over the universe $U-\{ u \}$. We can then add $u$ to all petals of the flower to get a petal over the universe $U$

This construction trivially satisfies the given properties.

---
# References
