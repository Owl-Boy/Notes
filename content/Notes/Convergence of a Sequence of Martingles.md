---
tags:
  - Note
  - Incomplete
---
202502151802

Tags : [[Intro to Martingales]]
# Convergence of a sequence of martingales
---
>[!theorem]
>Give a [[Filtered Probability Space]] $(\Omega, \mathcal F, \{ \mathcal F_{n} \}, P)$ a sequence $\{ M^{m} \}$ in the set of martingales, if:
>$$
>M_{n}^m \to M^n \text{ in } \mathbb L^1(P)
>$$
>Then $M$ is also a martingale.

The proof is fairly straightforward
$$
\begin{align}
E[\![ |E[\![X^m \mid \mathcal G]\!] - E[\![X \mid \mathcal G]\!]| ]\!] & =E[\![|E[\![(X^m-X) \mid \mathcal G]\!]|]\!] \\
&\leq E[\![E[\![|X^m-X|\mid \mathcal G]\!]]\!] \\
&= E[\![|X^m-X|]\!] \\
&= 0
\end{align}
$$

Applying this to $M^m_{n+1}$ wrt $\mathcal F_{n}$ gives us that $M$ is also a martingale.

---
# References