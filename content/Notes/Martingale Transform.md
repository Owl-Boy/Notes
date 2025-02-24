---
tags:
  - Note
  - Incomplete
---
202502152302

Tags : [[Intro to Martingales]]
# Martingale Transform
---
>[!definition]
>Let $M = \{ M_{n} \}$ be a martingale and $U = \{ U_{n} \}$ be a predictable sequence of random variables. The process $Z = \{ Z_{n} \}$ defined by $Z_{0}= 0$ and for$n\geq 1$
>$$
>Z_{n}  = \sum_{k=1}^n U_{k}(M_{k} - M_{k-1})
>$$
>is called a *Martingale Transform* of $M$ by the sequence $U$.

>[!theorem]
>If $M=\{  M_{n} \}$ is a martingale and $U =\{ U_{n} \}$ is a predictable process such that:
>$$
>E[\![|M_{n}U_{n}|]\!] < \infty \text{ for all } n\geq 1
>$$
>Then the martingale transform of $M$ by $U$ is also a martingale.

The proof is straightforward manipulation
$$
\begin{align}
E [\![U_{n}(M_{n}- M_{n-1}) \mid \mathcal F_{n-1}]\!] &= E[\![U_{n}M_{n} \mid \mathcal F_{n-1}]\!] - E[\![U_{n}M_{n-1} \mid \mathcal F_{n-1}]\!] \\
&= U_{n}E[\![M_{n} \mid \mathcal F_{n-1}]\!] - U_{n}M_{n-1} \\
&= U_{n}M_{n-1} - U_{n}M_{n-1} \\
&=0
\end{align}
$$
Which implies $Z_{n}$ is a martingale.

>[!attention]
>For a sub-martingale, we also need that $E[\![M_{n-1}U_{n}]\!]$ to be finite.

---
# References
