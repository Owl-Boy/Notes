---
tags:
  - Note
---
202508201608

Tags : [[Homotopy Type Theory]]
# Product types respect n-truncations
---
>[!theorem]
>Let $n\geq -2$, and let $A:\cal U$ and $B:A\to\cal U$. If for all $a:A, B(A)$ is an $n$-type then $\prod_{a:A}B(a)$ is also an $n$-type.

For $n=-2$, the result is in [[Some Contractible Types]].
For the inductive step, assume everything is an $n+1$-type. Then given $f,g$ we need to show that they are $n$-types. By [[Higher Groupoid Structure of Pi Type|Function Extensionality]] and closure of $n$-types under equivalence, it suffices to show that $\prod_{x:A}(f(a)=g(a))$ is an $n$-type which we have by induction.

---
# References
- [[n-Types]]
- [[Some Contractible Types]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]