---
tags:
  - Note
---
202506261606

Tags : [[Homotopy Type Theory]]
# Identity System
---
>[!definition]
>An **identity system** over a type $A$ is a type family $R:A \to A \to \cal U$ equipped with a function $r_{0}:\prod_{a:A}R(a,a)$ such that for any type family $D:\prod_{a, b:A}R(a, b)\to\cal U$ and $d:\prod_{a:A}D(a,a,r_{0}(a))$, there exists a function $f:\prod_{a, b:A}\prod_{r:R(a, b)}D(a, b, r)$ such that $f(a,a,r_{0}(a))=d(a)$ for all $A$.
>

>[!theorem]
>For $R:A\to A\to\cal U$ equipped with $r_{0}:\prod_{a:A}R(a,a)$, then the following are logically equivalent:
>1. $(R, r_{0})$ is an **identity system**.
>2. For all $a_{0}:A$ the pointed predicate $(R(a_{0}),r(a_{0}))$ is a [[Pointed Predicates and maps|pointed predicate]] at $a_{0}$.
>3. For any $S:A\to A\to\cal U$ and $s_{0}:\prod_{a:A}S(a,a)$ the type
>   $$
>   \sum_{( g:\prod_{(a, b):A}R(a, b)\to S(a,b))}\prod_{(a:A)}g(a,a,r_{0}(a))=s_{0}(a)
>   $$
>   is contractible.
>4. For any $a, b:A$ the map $\text{transport}^{R(a)}(-, r_{0}(a)):(a=_{A}b)\to R(a, b)$ is an equivalence.
>5. For any $a:A$ the type $\sum_{b:A}R(a, b)$ is contractible.

The equivalence between the first 2 points is precisely the equivalence between [[Path Induction]] and [[Based Path Induction]].

The equivalence with point 4 and point 5 follows from [[Identity System at a point]].

proof for equivalence for point 3 is also similar, if we fix an $a$, then we get it form [[Identity System at a point]] and then we use the theorem in [[Some Contractible Types]].

---
# References
- [[Identity System at a point]]
- [[Contractible Types]]
- [[Some Contractible Types]]
- [[Path Induction]]
- [[Based Path Induction]]
- [[Identity Type]]
- [[Pointed Predicates and maps]]