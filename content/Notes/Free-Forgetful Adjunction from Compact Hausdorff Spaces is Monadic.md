---
tags:
  - Note
---
202510171510

Tags : [[Category Theory]]
# Free-Forgetful Adjunction from Compact Hausdorff Spaces is Monadic
---
A topological space can be defined as a set $X$ endowed with a closure operator $\overline {(-)}:PX \to PX$ such that the following properties hold
$$
\begin{matrix}
\overline \emptyset = \emptyset & \quad & A \subseteq\overline A & \quad & \overline {\overline A}=\overline A & \quad & \overline {A \cup B}=\overline A\cup  \overline B
\end{matrix}
$$
A function $f$ is continuous if $f(\overline A) \subseteq\overline{f(A)}$ and is called **closed** if the equality holds. All continuous functions between [[Compactness|Compact]] [[Hausdorff Property|Hausdorff]] [[Topological Spaces|Spaces]] are closed.

Consider an [[Equalizers and Coequalizers|absolute coequalizer]] diagram in $\text{Set}$.
$$
X\underset g{\overset{f}\rightrightarrows}Y\overset h\twoheadrightarrow Z
$$
The powerset functor preserves this, giving rise to the following diagram:
![[Pasted image 20251017153553.png|300]]

Since $f$ and $g$ are maps of hausdorff spaces, these functions make the diagram commute.

The induced function defines a closure operator on $Z$ so that it makes $Z$ a topological space, as $h$ is surjective, continuous and closed. By our categorization of compact hausdorff spaces, we get a unique coequalizer map defined in $\text{cHaus}$. 

To see that $h$ has the universal property, we must prove that the right square commutes:
![[Pasted image 20251017154603.png|300]]

This is direct from the fact that $h_{*}$ is an epimorphism.

---
# References
- [[Compactness]]
- [[Hausdorff Property]]
- [[Topological Spaces]]
- [[Monads and Comonads]]