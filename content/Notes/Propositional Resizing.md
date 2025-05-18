---
tags:
  - Note
  - Incomplete
---
202505172205

Tags : [[Homotopy Type Theory]]
# Propositional Resizing
---
With [[Sub-Types]] defined, given a universe $\cal U$ one can define the following sub-universes:
$$
\begin{align}
\text{Set}_{\cal U} &:\equiv \{ A:\mathcal U \mid \text{is-Set} (A)\}\\
\text{Prop}_{\cal U} &:\equiv \{ A:\mathcal U \mid \text{is-Prop} (A)\}
\end{align}
$$
From this [[Sub-Types#^2d5f48|lemma]], we can say that $(A, s) =_{\text{Set}_{\cal U}}B(t)$ is equivalent to $A=B$, hence we will above the notation a lot. 

Since the universes are cumulative, we also have:
$$
\begin{align}
\text{Set}_{\cal U_{i}} & \to \text{Set}_{\cal U_{i+1}} \\
\text{Prop}_{\cal U_{i}} & \to \text{Prop}_{\cal U_{i+1}} 
\end{align}
$$
The first map cannot be an equivalence because of the same issues as naive set theory.
The second map is not automatically an equivalence but it is consistent with with everything discussed so far, hence we can consider adding the following axoim:

>[!axiom] Axiom : Propositional Resizing
>The map $\text{Prop}_{\cal U_{i}} \to \text{Prop}_{\cal U_{i+1}}$ is an equivalence

This states that any mere proposition $P$ in the universe $\mathcal U_{i+1}$ can be "resized" to a proposition in $\cal U_{i}$.

This actually holds is $\mathcal U_{i+1}$ satisfies $\text{LEM}$. This axiom will not usually be assumed.

The point of this is to create the type $\Omega$ of all mere proposition, which can be used to construct the power set given as
$$
\mathcal P(A) = A \to \Omega 
$$

---
# References
