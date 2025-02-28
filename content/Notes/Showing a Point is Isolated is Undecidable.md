---
tags:
  - Note
  - Incomplete
---
202502282102

Tags : [[Weighted Automata and Transducers]]
# Showing a Point is Isolated is Undecidable
---
>[!theorem]
>Given a $\theta$ and a [[Probabilistic Automata]] $\mathcal{A}$, it is undecidable to show is $\theta$ is an isolated cut point of $A$.

We are going to reduce a variant of [[Post Correspondence Problem]] to this problem.

>[!question]
>Given $f, g$, is the set $\{ f(w) \land g(w) \mid w \in \Sigma^* \}$ finite?
>Here $f(w)\land g(w)$ be the longest common prefix of the words.

If there are infinite in $\{ f(w) \land g(w) \}$, then one can find a word for any unbounded set in it. Hence $\frac{1}{2}f + \frac{1}{2}(1-g)$ can get arbitrarily close to $\frac{1}{2}$.

If there are only finitely many words, let $k$ be length of the largest word, hence the $\frac{1}{2}f + \frac{1}{2}(1-g)$ will have a distance of at least $\frac{1}{2^k}$ from $\frac{1}{2}$. 

Since this variant of [[Post Correspondence Problem]] is undecidable, so is the problem.

---
# References
