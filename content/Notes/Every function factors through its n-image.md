---
tags:
  - Note
---
202510050210

Tags : [[Homotopy Type Theory]]
# Every function factors through its n-image
---
>[!lemma] 
>For every function $f:A\to B$, the canonical function $\tilde{f}:A\to\text{im}_{n}(f)$ is $n$-connected. This any function factors as an $n$-connected function followed by an $n$-truncated function.

We have that $A\simeq \sum_{b:B}\text{fib}_{f}(b)$. The function on the total space is induced by the canonical fiberwise truncation
$$
\prod_{b:B} (\text{fib}_{f}(b)\to\|\text{fib}_{f}(b)\|_{n})
$$
Since each map in $\text{fib}_{f}(b)\to\|\text{fib}_{f}(b)\|_{n}$ is $n$-connected by [[Characterizing n connectedness using n-types]], $\tilde{f}$ is $n$-connected. We also know that projection $\pi_{1}$ is $n$-truncated since its fibers are equivalent to $n$-truncations to the fibers of $f$.

The process looks as follows:
- We have $f:A\to B$
- We get that the image of $f$ is $\sum_{b:B}\|\text{fib}_{f}(b)\|_{n}$
- And we get the following function: $a\mapsto \big(f(a), |(f(a), \text{refl}_{f(a)})|_{n}\big)$
	- This is an $n$-connected function $\tilde{f}$.
- We then take the first projection to get $f(a)$.
	- this is an $n$-truncated function as each fibre is an $n$-type.

---
# References
- [[Characterizing n connectedness using n-types]]
- [[n-image]]
- [[n-truncated functions]]