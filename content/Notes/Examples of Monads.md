---
tags:
  - Example
---
202507302107

Tags : [[Category Theory]]
# Examples of Monads
---
>[!example]
>The covariant powerset functor $P:\text{Set}\to\text{Set}$ is also a monad. The unit $\eta_{A}:A\to PA$ sends an element to the singleton subset. The multiplication $\mu_{A}:P^2A\to PA$ takes the union of a set of subsets. Naturality of the unit with respect to a function $f:A\to B$ makes use of the fact that $f_{*}:PA\to PB$ is the direct image function. Naturaily of the multiplication maps makes use of [[Corollaries of RAPL]].

>[!example]
>There is a monad $-\times \mathbb{N}:\text{Set}\to\text{Set}$. This can be thought of as adding a second component of an element as a discrete time variable. The unit $A\to A\times \mathbb{N}$ is defined by $a \mapsto(a,0)$ and the multiplication $A\times \mathbb{N}\times \mathbb{N}\to A\times \mathbb{N}$ is defined by $(a,m,n)\mapsto(a,m+n)$. 

>[!example]
>The **Giry Monad** acts on the category $\text{Meas}$ of [[Measure Space|measurable spaces]] and [[Measurable Functions]]. The **Giry monad** sends a measurable space $A$ to the measurable space $\text{Prob}(A)$ of [[Probability|probabilites]] on $A$, equipped with the smallest $\sigma$-algebra so that for each measurable subset $X \subseteq A$, the evaluation function $\text{ev}_{X}:\text{Prob}(A)\to I$ is measurable. The unit is the measurable function $\eta_{A}:A\to\text{Prob}(A)$ that sends each element $a \in A$ to the dirac measure which assigns a subset the probability $1$ if it contains $A$ and $0$ otherwise. 
>
>The definition of multiplication is using integration as follows: Let $\rho:\text{Prob}(\text{Prob}(\Omega))$ then $\eta_{\Omega}(\rho)$ is defined as:
>$$
>\eta_{\Omega}(\rho)(A) = \int_{\text{Prob}(\Omega)} \text{ev}_Ad\rho
>$$
>


---
# References
- [[Monads and Comonads]]
- [[Examples of Monads from Adjunctions]]
- [[Corollaries of RAPL]]
- [[Measure Space]]
- [[Measurable Functions]]
- [[Probability]]