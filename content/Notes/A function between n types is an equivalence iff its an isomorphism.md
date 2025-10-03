---
tags:
  - Note
---
202509242109

Tags : [[Homotopy Type Theory]]
# A function between n types is an equivalence iff its an isomorphism
---
>[!Lemma]
>Let $B$ be an $n$-type and let $f:A\to B$ be a function. Then the induced function $g:\|A\|_{n}\to B$ is an equivalence iff $f$ is $n$-connected.

By lemma discussed in [[Characterizing n connectedness using n-types]], the function $|-|_{n}$ is $n$-connected, the by [[if f an n connected, then g is n connected iff g(f) is n connected]], we hvae that $g$ is $n$-connected iff $f$ is $n$-connected.

But $g$ is a function between $n$-types, so its fibres are also $n$-types. Thus $g$ is $n$-connected iff it is an equivalence.

---
# References
- [[Characterizing n connectedness using n-types]]
- [[if f an n connected, then g is n connected iff g(f) is n connected]]
