---
tags:
  - Note
---
202506261506

Tags : [[Homotopy Type Theory]]
# Identity Systems at a Point
---
>[!definition]
>An **Identity System** at $a_{0}$ is a pointed predicate $(R, r_{0})$ such that for any type family $D: \prod_{a:A}R(a) \to\cal U$ and $d:D(a_{0}, r_{0})$, there  is a function $f: \prod_{a:A}\prod_{r:R(a)}D(a, r)$ such that $f(a, r_{0})=d$. 

>[!theorem]
>For a pointed predicate $(R,r_{0})$ over $(A,a_{0})$, the following are equivalent.
>- $(R, r_{0})$ is an [[Pointed Predicates and maps|Identity System]] at $a_{0}$.
>- For any pointed predicate $(S, s_{0})$ the type $\text{ppmap}(R, S)$ is [[Contractible Types|contractible]].
>- For any $b:A$, the function $\text{transport}^R(-,r_{0}):a_{0}=b\to R$ is an equivalence.
>- The type $\sum_{a:A}R(a)$ is [[Contractible Types|contractible]].

Note that the first 3 points are similar to the theorem in [[Some ways to Characterize Homotopy W types]].

Assuming point 1, Let $(S, s_{0})$ be a pointed predicate and define $D(a, r):\equiv S(a)$ and $d:\equiv s_{0} :S(a_{0})$. Then there is a function $f:\prod_{a:A}R(a)\to S(a)$ such that $f(a_{0},r_{0})=s_{0}$. Thus $\text{ppmap}(R, S)$ is inhabited. Now suppose $(f,f_{r})$ and $(g, g_{r}):\text{ppmap}(R, S)$. Then we can define $D(b, r):\equiv f(b, r)=g(b, r)$. and we can define $d:\equiv f_{r}\cdot g_{r}^{-1}: f(a_{0},r_{0})=s_{0}=g(a_{0},r_{0})$.  Since $(R, r_{0})$ is an identity system, we have it for every $a:A$, and then by function extensionality we get $(f,f_{r})=(g,g_{r})$.

Assuming 2, Define $S(b):\equiv a_{0}=b$ with $s_{0}:\equiv\text{refl}_{a_{0}}:S(a_{0})$. Then $(S,s_{0})$ is a pointed predicate and we have $\lambda b.\lambda p.\text{transport}^R(p, r):\prod_{a:A}S(a)\to R(a)$. So given any type family $D$ we can have a map from $S$ making $S$ an identity system too, This $R$ and $S$ are isomorphic.

Assuming 3, we get 4 from [[Some Contractible Types#^4248c0]].

Assuming 4, Let $D$ be of type $\prod_{a:A}R(A)\to\cal U$ and $d:D(a_{0},r_{0})$ we can also express $D$ as the family $D':\left( \sum_{a:A}R(A) \right)\to\cal U$. But we have that $\sum_{a:A}R(a)$ is contractible, so we have 
$$
p:\prod_{u:\sum_{b:A}R(b)} (a_{0},r_{0})=u
$$
But since path type of contractible types is contractive, we get $p((a_{0},r_{0}))=\text{refl}_{(a_{0},r_{0})}$. We can now define $f(u):\equiv\text{transport}^{D'}(p(u), d)$, giving us $f:\prod_{u:\sum_{b:A}R(b)}D'(u)$ or equivalently $\prod_{a:A}\prod_{r:R(a)}D(a, r)$. So we have
$$
f(a_{0},r_{0})\equiv \text{transport}^{D'} p(((a_{0},r_{0})), d)=\text{transport}^{D'}(\text{refl}_{(a_{0},r_{0})}, d)=d 
$$
So point 1 holds.

---
# References
- [[Pointed Predicates and maps]]
- [[W-Types]]
- [[Some ways to Characterize Homotopy W types]]
- [[Transport]]
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Identity Type]]
- [[Identity System]]