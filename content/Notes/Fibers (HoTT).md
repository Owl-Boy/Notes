---
tags:
  - Note
---
202505231705

Tags : [[Homotopy Type Theory]]
# Fibers
---
>[!definition] 
>The **Fiber** of a map $f:A\to B$ over the point $b:B$ is 
>$$
>\text{fib}_{f}(B) :\equiv \sum_{a:A} f(a)=_{B}b
>$$

The [[Higher Groupoid Structure of Sigma Type]] and [[Higher Groupoid Structure of Pi Type]] and [[Higher Groupoid Structure of Identity Types]] give the following lemma:
>[!lemma]
>For any $f:A \to B$ and $b:B$ and $(x, p), (x',p'):\text{fib}_{f}(b)$ we have 
>$$
>(x, p) = (x', p') \simeq \left( \sum_{\gamma:x=x'} f(\gamma)\cdot p'=p \right)
>$$

---
# References
- [[Higher Groupoid Structure of Sigma Type]]
- [[Higher Groupoid Structure of Pi Type]]
- [[Higher Groupoid Structure of Identity Types]]