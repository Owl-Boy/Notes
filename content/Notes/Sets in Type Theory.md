---
tags:
  - Note
---
202505141805

Tags : [[Homotopy Type Theory]]
# Sets in Type Theory
---
The collections in Homotopy Type Theory work like infinity groupoids, which in general is different from sets. There is a subclass of infinity groupoids, which are the discrete groupoids which are determined by a set of objects and only identity morphisms, and only identity higher-morphisms, topologically these would be sets with the discrete topology.

We define sets with no non-trivial "higher homotopy" information. Luckily, everything in hott is continuous and functorial, so it suffices to ask for the base case:

>[!definition]
>A set is a type $A$ such that for all $x,y:A$ and $p,q:x=y$ we have $p=q$.
>
>More precisely, we define a proposition $\text{is-Set}$ to be the type
>$$
>\text{is-Set}(A) :\equiv \prod_{x, y: A} \prod_{p,q: x=_{A}y} p=q
>$$

>[!example] [[Examples of Sets in Type Theory|Here are some Examples]].

>[!lemma]
>If $A$ is a set, then any identity type over $A$ is also a set

This is precisely what we refered to when we used the word "lucky".
Say $f: \text{is-Set}(A)$, that it takes 2 elements of $A$, 2 paths between them, and states they are equal, that is: $f(x,y,p,q):p=q.$ 

We now fix $x,y,p$ and define $g(q):\prod_{q:x=y}p=q$ by $g(q) = f(x,y,p,q)$, then for any $r:q=q'$ we have $\text{apd}_{g}(r):r_{*}(g(q))=g(q')$ but that just becomes $g(q) \cdot r=g(q')$, hence for any $r,s: p=q$ we have $g(q)\cdot r = g(q') = g(q)\cdot s$, so we get $r=s$.

---
# References
- [[Set Theory]]
- [[Identity Type]]