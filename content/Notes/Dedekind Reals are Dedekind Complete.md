---
id: Dedekind Reals are Dedekind Complete
aliases:
  - Dedekind Reals are Dedekind Complete
tags:
  - Note
  - Incomplete
---
202602172319

Tags : [[Homotopy Type Theory]]
# Dedekind Reals are Dedekind Complete
---
We say that an ordered field is admissible for $\Omega$ if the ordering map $<$ on $F$ is a map $< :F\to F\to \Omega$.

> [!LEM]
> Every archimedean ordered field which is admissible for $\Omega$ is a subfield of $\mathbb R_d$

Let $F$ be an archimedean ordered field and $x:F$, then we define $L_x$ and $U_x$ in the typical way.

This is a dedekind cut on the field $F$, giving and embedding of $F$ in $\mathbb R_d$. This will be a field embedding.

> [!LEM] 
> If $F$ is admissible for $\Omega$ then so is its dedekind completion.

Let $\bar F$ be the dedekind completion of $F$, the strict order is defined in a way similar to that of $\mathbb R_d$, and the lemma holds as long as $\Omega$ is closed under conjunction and countable existentials, which we have assumed from the start.

The trivial application of these 2 lemma is the following theorem:
> [!THM]
> Dedekind Reals are Dedekind Complete

Consider $f:\mathbb R\leftrightarrows \bar{\mathbb R}:g$. First consider $h=f;g:\mathbb R\to\mathbb R$.

We have $\forall (q:\mathbb Q), h(q)=q$.

Given $r:\mathbb R$ we have $L_r(q) \Leftrightarrow q<r\Leftrightarrow h(q)<h(r)\Leftrightarrow q < h(r) \Leftrightarrow L_{h(r)}(q)$. But since everything here is a mere proposition, all of them are equal, and by function extensionality we have $L_r=L_{h(r)}$ so we are done.

---
# References
- [[Dedekind Reals (HoTT)|Dedekind Reals]]
- [[Dedekind Reals are weakly linearly ordered]]
