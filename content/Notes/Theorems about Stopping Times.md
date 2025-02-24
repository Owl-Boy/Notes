---
tags:
  - Note
---
202502182302

Tags : [[Intro to Martingales]]
# Theorems about Stopping Times
---
>[!theorem]
>let $M=\{ M_{n} \}$ be a martingale, then $N=\{ M_{n\land \tau} \}$ is also a Martingale

The idea is that for all regions with new values, the martingale $N$ sort of evolves;
- $N_{0}=M_{0}$
- $N_{n+1} = N_{n} + I_{\tau>n}(M_{n+1}-M_{n})$
- $N_{n} = \sum_{i=1}^nI_{\{ \tau>i-1 \}}(M_{i}-M_{i-1})$

which is a martingale transform, so we are done.

---
>[!theorem]
>$M$ is a martingale if and only if for any bounded stop time $\tau$ 
>$$
>E[\![M_{\tau}]\!] =E[\![M_{0}]\!]
>$$

If $M$ is a martingale, then the previous theorem directly gives one direction.

If we assume for all bounded stop times $\tau$, $E[\![M_{\tau}]\!] =E[\![M_{0}]\!]$.
We now need for show that for any $n$ and for any $A\in\mathcal F_{n}$ we have 
$$
E[\![M_{n+1}I_{A}]\!]=E[\![M_{n}I_{A}]\!]
$$

To do so, let $\tau_{1}=(n+1)I_{A} + nI_{A^c}$ then you get 
$$
E[\![M_{n+1}I_{A} + M_{n}I_{A^c}]\!]=E[\![M_{0}]\!]
$$
And we define $\tau_{2} = n$ so we get
$$
E[\![M_{n}I_{A} + M_{n}I_{A^c}]\!]=E[\![M_{0}]\!]
$$
the difference of the 2 equation proves the theorem.

---
# References
