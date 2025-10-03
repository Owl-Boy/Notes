---
tags:
  - Note
  - Incomplete
---
202509231309

Tags : [[Homotopy Type Theory]]
# n-connected types
---
An $n$-connected type is a type which has no interesting homotopic information below dimension $n$. There is more general notion for functions:

>[!definition]
>A function $f:A\to B$ is said to be **$n$-connected** if for all $b:B$, the type $\|\text{fib}_{f}(b)\|_{n}$ is contractible:
>$$
>\text{conn}_{n}(f):\equiv \prod_{b:B}\text{isContra}(\|\text{fib}_{f}(b)\|_{n})
>$$
>A type $A$ is $n$-connected if the unique function $A\to \mathbf{1}$ is $n$-connected, that is $\|A\|_{n}$ is contractible.

It is also fairly straightforward to show that category theoretically, $(-1)$  connectedness corresponds to essential surjectivity on objects, while $n$-connectedness implies yp t on $k$-morphisms for $k\leq n-1$.

We also have that a type $A$ is $(-1)$ connected iff its merely inhabited. It is $0$-connected then we can call it *connected*, and when it is $1$-connected, it can also be called *simply connected*.

---
# References
- [[Truncation]]
- [[retract of an n-connected function is n-connected]]
- [[if f an n connected, then g is n connected iff g(f) is n connected]]