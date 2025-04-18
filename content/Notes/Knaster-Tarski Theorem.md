---
tags:
  - Example
---

202404031225

tags : [[Order Theory]]

#  Knaster-Tarski Theorem
---
>[!Theorem] 
>Let $(L, \le)$ be a [[Complete Lattice]] and $f : L \to L$ be a monotonous function, then the set of fixed points of $f$ also form a complete lattice under $\le$.

>[!tip] Intuition
>The proof goes by showing existence of fixed points, which is done by showing a non-empty set that is closed under $f$ and contains its supremum and infemum.

Let $S = \{ x \mid f(x) \leq x \}$ and let $s = \bigwedge S$ and we claim that $s$ is a fixed point of $f$.
We have that $s \leq x, \forall x\in S$, and since $f$ is monotone, $\forall x, f(s)\leq f(x)$, but $f(x) \leq x$ hence $f(s)$ is also a lower bound for $S$.

Hence $f(s) \leq s$, this $s \in S$. But $f(f(s)) \leq f(s)$, hence $f(s)\in S$, thus $s =f(s)$.

Since all fixed points are in $S$, we can claim that $s$ is the least fixed point $f$. By a similar argument one can also show that there exists a greatest fixed point.

With the proof of existence of fixed points, let $F$ be the set of all fixed points of the space. We let $s$ be the smallest fixed point and $l$ be the largest fixed point.

>[!tip] Intuition
>In the next part of the proof, we take a subset of the set off fixed points, and show that we can find a sub-complete lattice which contains all bigger that it, and hence its least fixed point will be the supremum of the set.

Let $W \subseteq F$ and let $w = \bigvee W$. We have that $f(w) \geq w$, this is because $w \geq w_{i}\in W$, so $f(w) \geq f(w_{i})=w_{i}$. Thus we have $f([w, l]) \subseteq [w, l]$.

But $[w, l]$ form a complete lattice and using the above steps we can find a least fixed point of $[w, l]$, which will be the supremem of $W$ in $F$. Similarly we can show that every set will also have in infemum.

---
# Related
