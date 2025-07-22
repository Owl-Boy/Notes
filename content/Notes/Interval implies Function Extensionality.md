---
tags:
  - Note
  - Incomplete
---
202507131607

Tags : [[Homotopy Type Theory]]
# Interval implies Function Extensionality
---

>[!lemma]
>Let $f,g:A\to B$ are two function such that $f(x)=g(x)$ for every $x$ then $f=g$ in the type $A\to B$.

We need to build an element of type $\prod_{x:A}f(x)=g(x)$. So for all $x:A$ we define a function. For all $x:A$ we define $\tilde{p}_{x}:I\to B$ give by
$$
\begin{align}
\tilde{p}_{x}(0_{I}) & :\equiv f(x) \\
\tilde{p}_{x}(1_{I}) & :\equiv g(x) \\
\tilde{p}_{x}(\text{seg}) & :\equiv p(x) 
\end{align}
$$
We now define $q:I\to (A\to B)$ by
$$
q(i):\equiv\lambda x.\tilde{p}_{x}(i)
$$
Then we have $q(0_{I})$ is the function $f$ and $q(1_{I})$ is the function $g$ so we get $q(\text{seg}):f=_{(A\to B)}g$.

>[!todo] Proof coming soon


---
# References
- [[Higher Groupoid Structure of Pi Type|Function Extensionality]]
- [[Interval (HoTT)|Interval]]