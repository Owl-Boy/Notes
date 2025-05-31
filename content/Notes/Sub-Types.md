---
tags:
  - Note
---
202505172105

Tags : [[Homotopy Type Theory]]
# Sub-Types
---
Type families like $P:A \to\cal U$ can be regarded as *predicate* on the elements of $A$. For any $a:A$  we get that $P(a)$ is a type, and we can say that $a$ satisfies the predicate $P$ if $P(a)$ is inhabited. 

In set theory, one can use the [[Axioms of ZFC#^799ea9|comprehension]] to construct subsets. The obvious analogue is $\sum_{a:A}P(a)$, that contains elements of the form $(a,p:P(a))$, where the first components would exactly make up the subset.

The slight issue with that is that given an $a$, there can be multiple elements in the type $P(a)$. To avoid that from happening, we simply put the restriction that $P$ is a [[Mere Propositions]].

>[!lemma]
>If $P:A \to\cal U$ is a type family such that $P(x)$ is a mere proposition for all $x:A$ then given $u,v:\sum_{x:A}P(x)$ if $\text{pr}_{1}(u)=\text{pr}_{2}(v)$, then $u=v$.

^2d5f48

To show that $u=v$ we show that $p_{*}(\text{pr}_{2}(u))=\text{pr}_{2}(v)$, but both of these are elements of $P(\text{pr}_{1}(v))$ which is a mere proposition, so they are equal.

Hence if $P:A \to\cal U$ is a family of mere propositions then, as an alternative notation for $\sum_{a:A}P(a)$ we may write:
$$
\{ a:A \mid P(a) \}
$$
We will call the a sub-type of $A$ and if $A$ is a set, then we may call this a subset, $P$ is sometimes also called a subset of $A$.

We may also say that $a\in \{ x:A \mid P(x) \}$ to refer to the mere proposition $P(a)$. If this holds, one can say that $a$ is a member of $P$. Given 2 subsets $P, Q$ we can write $P \subseteq Q$ if we have $\prod_{x:A} P(x) \to Q(x)$.

---
# References
- [[Axioms of ZFC]]
- [[Mere Propositions]]
- [[Sets in Type Theory]]