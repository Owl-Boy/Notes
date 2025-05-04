---
tags:
  - Note
  - Incomplete
---
202505041505

Tags : [[Category Theory]]
# Equivalence of Categories
---
>[!definition]
>An equivalence of categories $C, D$ consists of functors $F : C \leftrightarrows D:G$ together with the natural isomorphism $\eta:1_{C} \cong GF$ and $\epsilon: 1_{D} \cong FG$.
>We write this as $C \simeq D$

>[!example]
>Consider the categories $\mathbf{Set}^\delta$ and $\mathbf{Set}_{*}$, which are the categories of sets with functions and pointed sets with based point preserving paths. With the following functors:
>- $U:\mathbf{Set}_{*} \to \mathbf{Set}^\delta$ is the forgetful functor.
>- $(-)_{+}: \mathbf{Set}_{\delta} \to \mathbf{Set}^*$ which takes the set $S$  and takes it to $S \cup \{ S \}$ such that $S$ is considered to be the base point.
>
>We shall show that there is an equivalence between these 2 categories as witnessed by the functors, for that we need to define 2 natural isomorphism:
>- $\eta: 1_{\mathbf{Set}^\delta} \cong U(-)_{+}$
>- $\epsilon: 1_{\mathbf{Set}_{*}} \cong (U-)_{+}$
>Their components are:
>- $\eta: x \mapsto \text{id}_{x}$
>- $\epsilon: (X, x) \mapsto (X \setminus \{ x \} \cup \{ X \setminus \{ x \} \}, X \setminus \{ x \})$


---
# References
