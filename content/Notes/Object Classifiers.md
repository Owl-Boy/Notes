---
tags:
  - Note
---
202505292205

Tags : [[Homotopy Type Theory]]
# Object Classifiers
---
>[!theorem]
>Let $f:A \to B$, then the following diagram is a pull-back square:
>![[Pasted image 20250529221619.png|150]]
>where 
>$$
>\vartheta_{f} :\equiv \lambda a. (\text{fib}_{f}(f(a)), (a, \text{refl}_{f(a)}))
>$$

We have:
$$
\begin{align}
A &\simeq \sum_{b:B} \text{fib}_{f}(b) \\
& \simeq \sum_{b:B} \sum_{X:\cal U} \sum_{p:\text{fib}_{f}(b)=X} X \\
&\simeq \sum_{b:B} \sum_{X:\cal U}\sum_{x:X} \text{fib}_{f}(b) =X \\
&\simeq \sum_{b:B} \sum_{Y:\mathcal U_{\bullet}}\text{fib}_{f}(b)=\text{pr}_{1}(Y) \\
&\equiv B \times_{\cal U} U_{\bullet} 
\end{align}
$$

Which gives us the composite.
$$
\begin{align}
a&\mapsto (f(a), \text{refl}_{f(a)}) \\
&\mapsto (f(a), \text{fib}_{f}(f(a)),\text{refl}_{f(a)}, (a, \text{refl}_{f(a)}) ) \\
&\mapsto (f(a), \text{fib}_{f}(f(a)), (a,\text{refl}_{f(a)}), \text{refl}_{\text{fib}_{f}(f(a))})
\end{align}
$$
So we also get the homotopes: $f \sim \text{pr}_{1}\circ e$ and $\vartheta_{f}\sim \text{pr}_{2}\circ e$.
 


---
# References
- [[Pullbacks and Pushouts]]
- [[Uniqueness Principle for Sigma Types]]
- [[Homotopy(HoTT)]]
