---
tags:
  - Note
---
202505261305

Tags : [[Homotopy Type Theory]]
# Retracts 
---
>[!definition]
>We call a function $r: A\to B$ a **Retraction** if there exist a function $s:B\to A$ such that $r\circ s\sim \text{id}_{B}$. We would call $s$ here a **Section**. And we call $B$ a **Retract** of $A$.

>[!definition]
>A function $g:A \to B$ is said to be a **Retract** if there exists a function $f:X \to Y$ such that the following diagram commutes;
>![[Pasted image 20250526140449.png|200]] 
>with the following homotopies:
>- $R:r \circ s\sim\text{id}_{A}$
>- $R':r' \circ s'\sim\text{id}_{B}$
>- $L: f\circ s \sim s' \circ g$
>- $K: g \circ r \sim r'\circ f$
>- For every $a:A$ a path $H(a)$ witnessing the commutativity of the square:
>  ![[Pasted image 20250526140853.png|300]]

We describe functions with the same properties as their fibers, so we need to show:

>[!lemma] 
>If a function $g: A \to B$ is a retract of a function $f:X \to Y$, then $\text{fib}_{g}(b)$ is a retract of $\text{fib}_{f}(s'(b))$ for every $b:B$, where $s':B \to Y$.

^447d61

The diagram we get is:
$$
\sum_{a:A} g(a)=b \longrightarrow \sum_{x:X}f(x)=s'(b) \longrightarrow \sum_{a:A}g(a)=b
$$
The idea is to take elements of $a$ along $s$ and then down to $s'(b)$ like that.
Consider an element $(a, p)$ we send that element to: $(s(a), L(a) \cdot s'(p))$, call this function $\varphi_{b}$ 

For the next map, we need to send $s(a)$ back to $a$, and we will use $r$ for that,
we send $(x, q)$ to $(r(x),  K(x) \cdot r'(q) \cdot R'(x))$. Call this function $\psi_{p}$

So their composition becomes $(a, p) \mapsto (r(s(a)), K(s(a)) \cdot r(L(a) \cdot s'(p)) \cdot R'(s(a)))$. And we need to show $\psi_{p}\circ \varphi_{p} (a, p) = (a, p)$. So we need to show

$$
\prod_{(b:B)} \prod_{(a:A)} \prod_{(p:g(a)=b)} \psi_{b}(\varphi_{b}(a, p)) = (a, p)
$$
We can swap the first two $\Pi s$ and for some reason we can get
$$
\prod_{a:A}  (\psi_{g(a)}\circ\phi_{g(a)}) (a, \text{refl}_{g(a)})=(a, \text{refl}_{g(a)})
$$
And for any $a$ we need to show that the equality holds component wise, so we get.
We have $R(a):r(s(a))=a$, so for the other component we get
$$
R(a)_{*}(K(s(a))\cdot r'(L(a)\cdot s'(\text{refl}_{g(a)})) \cdot R'(g(a))) = \text{refl}_{g(a)}
$$
but this simplifies to 
$$
g(R(a))^{-1} \cdot K(s(a))\cdot r'(L(a)) \cdot R'(g(a)) = \text{refl}_{g(a)}
$$
The term witnessing this would be $g(R(a))^{-1}\cdot H(a)\cdot R'(g(a))$.

---
# References
- [[Retractions]]
- [[Homotopy(HoTT)]]