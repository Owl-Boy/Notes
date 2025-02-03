---
tags:
  - Note
aliases:
  - BNDP
---
202501310001

Tags : [[Finite Model Theory]]
# Bounded Number of Degrees Property
---
>[!lemma]
>For every relational vocabulary $\sigma$, there exists $2$ functions $f_{\sigma}$ and $g_{\sigma}:\mathbb{N} \to \mathbb{N}$ such that:
>1. For every $\mathfrak A \in \text{STRUCT}_{l}[\sigma]$, we have $\text{deg\_set}(\mathcal G(\mathfrak A)) \subset \{ 1\dots f_{\sigma}(l) \}$
>2. For every $\frak A$ with $\text{deg\_set}(\mathcal G(\mathfrak A)) \subseteq \{ 1\dots l \}$, we have $\mathfrak A \in \text{STRUCT}_{g_{\sigma}(l)}[\sigma]$.

Using the above we can define the following characterization:
>[!definition]
>Let $\sigma$ be a relational signature. An $m$-ary  query $Q$ with $m>0$, has the *bounded number of degree property* (BNDP) if there exists a function $f_{Q}: \mathbb{N} \to \mathbb{N}$ such that for every $l \geq 0$ and every $\mathfrak A\in \text{STRUCT}_{l}[\sigma]$
>$$
>|\text{deg\_set}(Q(\mathfrak A)) | \leq f_{Q}(l)
>$$

This definition is closely related to the locality concepts and its generally much easier to prove a violation of this property than the locality theorems.

---
# References
