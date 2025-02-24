---
tags:
  - Note
  - Incomplete
---
202502190002

Tags : [[Intro to Martingales]]
# Doob's Maximal Inequality
---
>[!theorem]
>Let $M$ be a martingale, then for $\lambda> 0$ and $n\geq 1$ one has:
>$$
>P(\max_{0\leq k\leq n}|M_{k}| >\lambda) \leq \frac{1}{\lambda}E[|M_{n}|1_{\max_{0\leq k\leq n }|M_{k}|\geq\lambda}]
>$$ 

Let $N_{k}=|M_{k}|$ be a sub-martingale.
Let 
$$
\tau = \inf \{ k:N_{k}>\lambda \}
$$
and we further get $\{ max_{0\leq k\leq n} N_{k}\leq\lambda\} \subseteq \{ \tau > n \}$. But we have that $S_{n} = T_{n}-T_{n\land \tau}$ is a sub-martingale with $S_{0}=0$ so $E[S_{n}] \geq 0$ which is the same as 
$$
E[S_{n}I_{\max_{0 \leq i \leq n} N_{k}>\lambda}]\geq0
$$
Expanding the definition of $S_{n}$ we get
$$
E[N_{n \land \tau}I_{\max_{0 \leq i \leq n} N_{k}>\lambda}]\leq E[N_{n}I_{\max_{0 \leq i \leq n} N_{k}>\lambda}]
$$
If we have the condition of the indicator functoin, we have that $\tau<n$ on that set, which means $N_{\tau}>\lambda$ so we have 
$$
N_{\tau \land n}I_{\max_{0 \leq i \leq n} N_{k}>\lambda} \geq \lambda I_{\max_{0 \leq i \leq n} N_{k}>\lambda}
$$
And we are done.

---
# References
