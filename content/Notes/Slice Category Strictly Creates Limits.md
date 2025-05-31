---
tags:
  - Note
  - Incomplete
---
202505301205

Tags : [[Category Theory]]
# Slice Category Strictly Creates Limits
---
>[!lemma]
>For any object $c:C$, the forgetful functor $\prod:c / C \to C$ strictly creates
>- All limits that $c$ admits, and
>- All connected colimits that $C$ contains.

Define a diagram $(K, \kappa):J \to c / C$ by defining a functor $K: J \to C$ along with a cone $\kappa:c \Rightarrow K$ with summit $c$. This can be written as
$$
K : J \xrightarrow{\;\;(K, \kappa)\;\;} c / C \xrightarrow{\quad\Pi\quad} C
$$
Given a limit cone $\lambda:l \Rightarrow C$, the cone $\kappa$ would factor through it using a unique morphism $t$. The map $t$ would thus be the limit element of $c/ C$.

For the second point, suppose $J$ is connected, and that $K$ admits a colimit $\mu:K \Rightarrow p$. We first lift along the functor $\Pi$. we do so by picking an object $j$ such that we have
$$
c\xrightarrow{\kappa_{j}} Kj \xrightarrow{\mu_{j}}p
$$
But since $J$ is connected, it does not depend on the choice of $j$.
Now given any co-cone in $c / C$, the underlying cone uniquely factors through $p$. And we can simply pull up factorization, and we are done.


---
# References
