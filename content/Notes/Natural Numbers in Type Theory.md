---
tags:
  - Note
---
202503282203

Tags : [[Homotopy Type Theory]]
# Natural Numbers in Type Theory
---
The elements of natural numbers are constructed using the constructors $0:\mathbb{N}$ and the successor operator $\text{succ}:\mathbb{N} \to \mathbb{N}$. One nice thing about this type is that here the notion of induction and recursion work in a familiar manner, this happens to be one of the essential properties of natural numbers that we want to preserve.

>[!note] Recursion Principle
>To construct a non-dependent function from $\mathbb{N}$ one needs to define a starting point $c_{0}:C$ and "next step" function $c_{s}:\mathbb{N} \to C \to C$, with the following definition:
>$$
>\begin{align}
>f(0) &:\equiv c_{0}\\
>f(\text{succ}(n)) &:\equiv c_{s}(n, f(n))
>\end{align}
>$$

We say that $f$ is defined by primitive recursion if it is defined this way, the following is an easy algorithm:
>[!example]
>We define the double, which takes a natural number and returns the double of that:
>$$
>\begin{align}
>f(0) &:\equiv 0 \\
>f(\text{succ}(n)) &:\equiv \text{succ}(\text{succ}(f(n)))
>\end{align}
>$$

We can define multi-variable function by allowing $C$ to be a function and and defining a curried version of the function as follows:
>[!Example]
>$$
>\begin{align}
>c_{0} &: \mathbb{N} \to \mathbb{N}  \\
>c_{0}(n) &:\equiv n \\
>c_{s} &: \mathbb{N} \to (\mathbb{N} \to \mathbb{N}) \to (\mathbb{N} \to \mathbb{N}) \\
>c_{s}(m, g)(n) &:\equiv succ(g(n))
>\end{align}
>$$
>Then we obtain $\text{add}:\mathbb{N} \to \mathbb{N}\to \mathbb{N}$ satisfying the following equality
>$$
>\begin{align}
>\text{add}(0, n) &\equiv n \\
>\text{add}(\text{succ}(m), n) &\equiv \text{succ}(add(m, n))
>\end{align}
>$$

^5e069a

We can package the previous in the following recursor:
$$
\text{rec}_{\mathbb{N}} : \prod_{C:\cal U}\mathbb{N} \to (\mathbb{N} \to C \to C) \to (\mathbb{N} \to C)
$$
With the defining function
$$
\begin{align}
\text{rec}_{\mathbb{N}}(C, c_{0}, c_{s}, 0) &:\equiv c_{0} \\
\text{rec}_{\mathbb{N}}(C, c_{0}, c_{s}, \text{succ}(n)) &:\equiv c_{s}(n, \text{rec}_{\mathbb{N}}(C, c_{0}, c_{s}, n))
\end{align}
$$
>[!note] Induction Principle
>Now we extend the recursion principle to dependently typed functions. Thus assume a family $C : \mathbb{N} \to\cal U$, an element $c_{0}:C(0)$ and a function $c_{s}:\prod_{n:\mathbb{N}} C(n)\to C(\text{succ}(n))$ with the following definitional equations
>$$
>\begin{align}
>f(0) &:\equiv c_{0} \\
>f(\text{succ}(n)) &:\equiv c_{s}(n, f(s))
>\end{align}
>$$
>Which can be packaged into the following induction principle:
>$$
>\text{ind}_{\mathbb{N}} : \prod_{C:\mathbb{N} \to\cal U} C(0) \to \left( \prod_{n:\mathbb{N}}C(n) \to C(\text{succ}(n)) \right) \to \prod_{n:\mathbb{N}}C(n)
>$$
>with the defining equations:
>$$
>\begin{align}
>\text{ind}_{\mathbb{N}} (C, c_{0}, c_{s}, 0) &:\equiv c_{0}\\
>\text{ind}_{\mathbb{N}} (C, c_{0}, c_{s}, \text{succ}(n)) &:\equiv c_{s}(n, \text{ind}_{\mathbb{N}}(C, c_{0}, c_{s}, n))
>\end{align}
>$$

We can use the above induction principle to state that if we can prove a property $P :\mathbb{N} \to \cal U$ for $n=0$ and we can show that if it holds for a number, it will hold for its successor, then we can prove it for all natural numbers

The proof is discussed in [[Addition is Associative (Type Theory)|Addition is Associative]].

---
# References
[[Addition is Associative (Type Theory)]]
[[Peano Axioms and Type Theory]]