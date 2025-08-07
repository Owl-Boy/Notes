---
tags:
  - Note
---
202507301607

Tags : [[Category Theory]]
# Monads and Comonads
---
>[!quote] Philip Wadler, fictional attribution to Philip Wadler
>A monad is just a monoid in the category of endofunctors, what's the problem?

>[!definition]
>A **monad** on a category $C$ consists of the following:
>- An endofunctor $T:C\to C$
>- A **unit** natural transformation $\eta:1_{C}\Rightarrow T$
>- A **multiplication** natural transformation $\mu:T^2\Rightarrow T$
>
>so that the following diagrams commute in $C^C$:
>![[Pasted image 20250730165306.png|450]]

This construction is very very similar to the definition of [[Monoids]], in fact this forms a monoidal object in the category of endofunctors on $C$ where multiplication is composition.

>[!definition]
>A **comonad** on $C$ is a monad on $C^\text{op}$: explicityly, a comonad consists of an endofunctor $K:C\to C$ together with natural transformation $\epsilon:K\Rightarrow 1_{C}$ and $\delta:K\Rightarrow K^2$ and the dual of the diagrams above commute.

---
# References
- [[Maybe Monad]]
- [[Functors]]
- [[Category Theory]]
- [[Monoids]]
- [[Examples of Monads]]
- [[Examples of Monads from Adjunctions]]
- [[Examples of Comonads]]