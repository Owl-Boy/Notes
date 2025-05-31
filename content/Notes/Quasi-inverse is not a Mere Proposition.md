---
tags:
  - Note
---
202505201305

Tags : [[Homotopy Type Theory]]
# Quasi-inverse is not a Mere Proposition
---
>[!lemma]
>There exists type $A,B$ and a functions $f:A \to B$ such that $\text{qinv}(f)$ is not a [[Mere Propositions|mere proposition]].

By [[Lemma 1 for Quasi-inverse is not a Mere Proposition|lemma 1]] it suffices to show that that there is a type $X$ such that $\prod_{x:X}(x=x)$ is not a mere proposition.

We define $X = \sum_{A:\cal U} \|\mathbf{2}=A\|$, and we show an element $f$ that is not equal to $x \mapsto \text{refl}_{x}$.

Let $a :\equiv (\mathbf{2},|\text{refl}_{2}| ):X$, and let $q:a=a$ to be the non-identity equivalence $e: \mathbf{2} \simeq \mathbf{2}$. We would now like to use [[Lemma 2 for Quasi-inverse is not a Mere Proposition|lemma 2]] to build $f$.
- For the first point, we know that $\mathbf{2}\simeq \mathbf{2}$ is a set, as $\mathbf{2}$ is a set. From the definition of $X$, equality in subsets and univalence, we get $(a=a) \simeq (\mathbf{2 \simeq 2})$ is also a set, so point 1 is satisfied.
- By the definition of equality, for any $(A, |p|)$ we have an element of $(A, |p|)=(\mathbf{2}, |\text{refl}_{\mathbf{2}}|)$.
- For the third point, not that all equivalences of $\mathbf{2}$ are either $\text{id}_{\mathbf{2}}$ or $e$.

Hence we can construct a function $f$ that sends $\mathbf{2}\mapsto e$ which is not the same as the function that sends $\mathbf{2} \mapsto \text{refl}_{\mathbf{2}}$. So we are done.

---
# References
- [[Functions as Equivalences]]
- [[Mere Propositions]]
- [[Univalence]]
- [[Lemma 1 for Quasi-inverse is not a Mere Proposition]]
- [[Lemma 2 for Quasi-inverse is not a Mere Proposition]]
- [[Uniqueness Principle for Sigma Types]]