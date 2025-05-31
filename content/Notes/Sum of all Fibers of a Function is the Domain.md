---
tags:
  - Note
---
202505292105

Tags : [[Homotopy Type Theory]]
# Sum of all Fibers of a Function is the Domain
---
>[!lemma]
>For any function $f:A \to B$, we have $A \simeq \sum_{b:B}\text{fib}_{f}(b)$

$$
\begin{align}
\sum_{b:B}\text{fib}_{f}(b) &\equiv \sum_{b:B} \sum_{a:A} f(a)=b \\
&\simeq \sum_{a:A} \sum_{b:B} f(a)=b \\
&\simeq A
\end{align}
$$
The step from line 2 to line 3 happens because $\sum_{b:B}f(a)=b$ is contractible.

---
# References
- [[Fibers (HoTT)]]
- [[Contractible Types]]
- [[Functions as Equivalences]]