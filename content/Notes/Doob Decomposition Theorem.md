---
tags:
  - Note
  - Incomplete
---
202502151902 

Tags : [[Intro to Martingales]]
# Doob Decomposition Theorem
---
The Doob decomposition theorem gives a unique decomposition for every adapted process as the sum of a [[Predicable Process]] and a [[Martingales|Martingale]].

>[!theorem] Doob's Decomposition Theorem
>Let $\mathcal{A} = (\Omega, \mathcal F, P)$ be a probability space. $\{ \mathcal F_{n} \}$ be a filtration of $\mathcal F$. Let $X= \{ X_{n} \}$ be an adapted process with $E[\![X_{i}]\!]< \infty$.
>
>Then there exists a martingale $M$ and an integrable predictable process $A$ starting at $A_{0} = 0$ such that $X_{i} = M_{i} + A_{i}$.

***Existence:***
We have that $M_{0} =X_{0}$ and 
Since $M$ is a martingale, we have that $E[\![M_{n+1}-M_{n}]\!]= 0$
So we can define $M_{n+1} = M_{n} + (X_{n+1} - E[\![X_{n+1} \mid \mathcal F_{n}]\!])$. This is clearly a martingale and we get $A_0 = 0$ while $A_{n+1} = A_{n} + (E[\![X_{n+1} \mid \mathcal F_{n}]\!] - X_{n})$, which is clearly predictable.

***Uniqueness:***
To prove uniqueness, let $X = M+A = M' + A'$.
Then $Y= M-M'=A'-A$ is a martingale.

But that would mean that $Y$ is both predictable process and a martingale. This would mean that $E[\![Y_{n} | \mathcal F_{n}]\!]=Y_{n}=Y_{n-1}$ for all $n$. And we have that $Y_{0}=A_{0}'-A_{0}=0$ so $Y_{n}=0$.

This shows the uniqueness.

---
# References
