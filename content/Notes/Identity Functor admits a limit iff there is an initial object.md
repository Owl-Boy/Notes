---
tags:
  - Note
---
202506141206

Tags : [[Category Theory]]
# Identity Functor admits a limit iff there is an initial object
---
>[!theorem]
>For any small category $C$, the identity functor  $1_{C}:C\to C$ admits a limit if and only if $C$ has an initial object.

Consider a limiting cone $\lambda_{c}:l\to c$. Here $l$ is a **weakly initial object**, that is it has at least 1 morphism to every other object.

We need to show that $\lambda_{c}$ is the only morphism from $l$ to $c$. 
Given any morphism $f:a\to b$, since $\lambda$ is a cone, we have $f\lambda_a=\lambda_{b}$, specifically pick an $f:l\to c$ we have $f\lambda_{l}=\lambda_c$. We now need to show that $\lambda_{l}$ is $\text{id}_{l}$.

Now for all $c$, consider $\lambda_{c}$ as a morphism in the diagram. then from the above argument we get $\lambda_{c}\lambda_{l}=\lambda_c$. That lets us factorize the cone through $\lambda_{l}$. But such factoriaztion are unique and is also possible through  $\text{id}$, hence $\lambda_{l}$ must be identity.

---
# References
- [[Small Categories]]
- [[Limits and Colimits]]