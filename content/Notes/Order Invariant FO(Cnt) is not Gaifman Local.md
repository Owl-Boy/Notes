---
tags:
  - Note
  - Incomplete
---
202504290404

Tags : [[Finite Model Theory]]
# $({FO(Cnt)} +<)_{\text{inv}}$ is not Gaifman Local
---
>[!theorem] 
>There exists queries in $({FO(Cnt)} +<)_{\text{inv}}$ that are not [[Gaifman-Locality|Gaifman Local]].

Let $\sigma=\{ E_{2}, P_{1} \}$. We call a $\sigma$-structure good, if the following conditions are satisfied:
1. $E$ has exactly 1 node of in-degree 0 and 1 node of out-degree 0. All other nodes have both in-degree and out-degree 1
2. $P$ contains the first element of the chain, but not the last. And for any vertex in $P$, it contains its predecessor.
3. $|P| < \log n$, where $n$ is the size of the universe.

The claim is that it is possible for to write a formula $\Phi_{\text{good}}$, which classifies all good structures in $(\text{FO(Cnt)} + < )_{\text{inv}}$.
Conditions $1$ and $2$ can be verified in $\text{FO}$.
For the 3rd condition it is sufficient to check if $j < \log k$ or equivalent $2^{ j } < k$. This is possible in $\text{FO(Cnt)}$ as dicussed in [[BIT is expressible in FO(+, *)]].

We now write the query $Q$:
$$
\text{If } \mathfrak A \text{ is good, return the transitive closure of }E \text{ restricted to } P.
$$
This is clearly not gaifman-local:

We first assume WLOG that elements of $P$ are before elements not in $P$, under $<$, otherwise we can always construct $<_{1}$ which agrees on pairs in $P^2$ and $\bar{P}^2$, but satisfy our condition.

Let $S \subseteq P$ with $S = \{ s_{1}, \dots , s_{m} \}$. Let $s_{j}$ be the $i_{j}^\text{th}$ element of $<$.

Define $a_{S}$ as the $p^\text{th}$ element of $A$ in $<$ where $\text{BIT}(p,i_{j})$ is true and is false on all other indexes. And because of our size restrictions on $P$, that is $|P| < \log n$, such an element always exists. So we can write the predicate $\text{Code}(u, v)$, where $v$ is of the form $a_{S}$ and $u\in S$.

We can now define the query by the formula $\exists z, \psi(x, y, z)$ where $\psi$ says $z$ codes the path between $x$ and $y$. That is 
- $\text{Code}(x, z)$ and $\text{Code}(y, z)$
- The element before $x$ and after $y$ does not belong to $z$,.
- For every other element $u$, $\text{Code}(u, z)$ implies its neighbours also satisfy it.
- $\text{Code}(\underline{\min}, z)$ holds iff $\underline{\min}=x$ and $\text{Code}(\underline{\max})$ never holds.
Clearly all of them are possible in $\text{FO(Cnt)}$.


---
# References
