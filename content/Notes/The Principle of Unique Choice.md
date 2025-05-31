---
tags:
  - Note
---
202505191805

Tags : [[Homotopy Type Theory]]
# The Principle of Unique Choice
---
We first note the following:
>[!theorem]
>If $P$ is a mere proposition, then $P\simeq \|P\|$

The direction from right to left is just the constructor for mere proposition. And since $P$ is a mere proposition, we can use the recursion principle to define a function from $\|P\| \to P$ by defining a function $P \to P$, which will be the identity function.

Now we can state the corollary:
>[!lemma]
>Suppose there is a type family $P:A \to\cal U$ such that
>- $P(x)$ is a mere proposition for each $x:A$
>- $\|P(x)\|$ is inhabited for each $x:A$
>
>Then one can construct a function of type $\prod_{x:A}P(x)$

The idea here is, if we know that $\|A\|$ holds, and we want to construct an element of $B$, we would want a function of type $A \to B$. But that would only be helpful if $B$ is a mere proposition.

Instead we can add structure to pick out an element by constructing a type family $Q:B \to\cal U$ such that $\sum_{x:B}Q(x)$ is a mere proposition. Now given a function $f:A \to B$, such that we can get $b$ such that $Q(b)$ holds. Thus we can make a function from $A \to \|\sum_{x:B}Q(x)\|$ and hence a function from $\|A\|$ it.

But note that $\sum_{x:B}Q(x)$ is a mere proposition, so its equal to its truncation, and then we can project to get an element of $b$.

---
# References
- [[Mere Propositions]]
- [[Dependent Pair Types|Sum Type]]