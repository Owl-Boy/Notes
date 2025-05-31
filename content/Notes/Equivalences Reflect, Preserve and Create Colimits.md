---
tags:
  - Note
---
202505241605

Tags : [[Category Theory]]
# Equivalences Reflect, Preserve and Create Colimits
---
>[!theorem]
>An equivalence of categories preserve, reflect and create all limits and colimits that are present it in its domain or codomain.

Equivalences are always fully faithful, and [[Fully Faithful Functors Reflect Limits and Colimits]]. 

Given a limit cone  $\lambda :c\Rightarrow K$ consider its image $\mu:Fc \Rightarrow FK$, which is also a cone, we need to show that it is a limit cone.

Consider any other cone $\mu': d' \Rightarrow FK$. Since $F$ is essentially surjective, consider an element $c'$ such that $Fc' \simeq d'$, and by fully faithful nature of $F$ we get that $c'$ is a cone over $K$ which factors through $\lambda$. This factoring can be pushed so that $F\lambda' :Fc'\Rightarrow FK$ . But that is isomorphic to the cone $\mu'$ so we are done. Hence equivalences preserve limits, and dually preserve colimits.

Now consider a limit $\mu: d \Rightarrow FK$, since $F$ is essentially surjective, there is an element $c$ such that $Fc \simeq d$, hence wlog assume $d=Fc$. From that consider the cone $\lambda:c \Rightarrow K$. Now consider any cone $\lambda':c'\Rightarrow K$, we push it down to get $\mu':Fc'\Rightarrow K$, which factorises through $\mu$ and we can simply push the factorization up. Hence equivalences create limits, and dually colimits.



---
# References
